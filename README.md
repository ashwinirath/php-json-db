# PHP JSON DB

PHP JSON DB is a simple, lightweight, and secure JSON-based database in PHP, developed by Ashwini Kumar Rath.

## Features

- Basic create, read, update, and delete (CRUD) operations.
- Data is stored in JSON format.
- All data is automatically encrypted and decrypted using the OpenSSL extension.
- Can load from and save to a file.

## Usage

```php
// Include the class
require_once 'JsonDB.php';

// Create a new database instance with your encryption key
$db = new JsonDB('your-encryption-key');

// Load data from a file
$db->loadFromFile('your-file.json');

// Put a value in the database
$db->put('key', 'value');

// Append a value to an array in the database
$db->append('key', 'value');

// Delete a value from the database
$db->delete('key');

// Save data to a file
$db->saveToFile('your-file.json');

Note: You should replace `'your-encryption-key'` and `'your-file.json'` with the actual encryption key and file name you're using.

