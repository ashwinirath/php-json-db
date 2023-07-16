# PHP JSON DB

PHP JSON DB is a simple, lightweight, and secure JSON-based database in PHP, developed by Ashwini Kumar Rath.

## Features

- Basic create, read, update, and delete (CRUD) operations.
- Data is stored in JSON format.
- All data is automatically encrypted and decrypted using the OpenSSL extension.
- Can load from and save to a file.

## Installation
To get started with **JsonDB**, you first need to include the JsonDB class in your PHP script:
```php
require_once 'JsonDB.php';
```

## Usage
### Creating a new JsonDB Instance
Create a new JsonDB instance with your data loaded from a file. JsonDB supports both plain and encrypted data storage.

```php
$filename = 'your-file.json';  // Replace with your filename
$encrypt = [false, '', ''];    // Replace with encryption details if required
$db = new JsonDB($filename, $encrypt);

The **$encrypt** array takes three elements:
1. A boolean representing whether encryption is enabled or not.
2. The encryption key is a string.
3. The encryption method (default is '**AES-256-CBC**').

For example, to enable encryption:
```php
$encrypt = [true, 'your-encryption-key', 'AES-256-CBC'];
$db = new JsonDB($filename, $encrypt);

### Basic Operations
**JsonDB** provides basic CRUD operations that you can use to manage your data.

1. **PUT**: To add or update a value in the database, use the **put** method:
```php
$db->put('key', 'value');

- **APPEND**: To append a value to an array in the database, use the **append** method:
``$db->append('key', 'value');

- **DELETE**: To delete a value from the database, use the delete method:
``$db->delete('key');

- **GET**: To get a value from the database, use the get method:
``$value = $db->get('key');

**Note:** Any changes made to the database (put, append, delete) are automatically saved to the file.

### File Operations
JsonDB also provides methods to manually load from and save to a JSON file.
- **LOAD**: To manually load data from the file into the database, use the **loadFromFile** method:
``$db->loadFromFile();

- **SAVE**: To manually save the data in the database to the file, use the **saveToFile** method:
``$db->saveToFile();

## License
JsonDB is released under the [MIT License](https://github.com/ashwinirath/php-json-db/blob/main/LICENSE).


