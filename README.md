# is-nx-romfs-file

Checks if the file path is an nx romfs file (e.g. `.romfs`, `.bin`). It does not read the complete file nor does it depend on the file extension

### Installation

<!-- Install with [npm](https://www.npmjs.com/):

```sh
$ npm install is-nx-romfs-file --save
``` -->

### Usage

```javascript
var ROMFS_FILE = require("is-nx-romfs-file");

// If a valid nx romfs file is provided and exists at path specified
ROMFS_FILE.isNxRomfs("temp.romfs", function (err, is) {
	if (err) {
		console.log("Error while checking if file is nx romfs: " + err);
	} else {
		console.log("Given file is nx romfs: " + is);
	}
});
//=> Given file is nx romfs: true

// If a valid nx romfs file is provided and exists at path specified
ROMFS_FILE.isNxRomfsSync("temp.romfs");
//=> true
```

### Clone the repo

```bash
$ git clone https://github.com/Migushthe2nd/is-nx-romfs-file.git
```

### API

#### isNxRomfs(path, cb)

This is asynchronous API for checking if file is an nx romfs. This API takes two parameters:

1. File path which needs to be checked and
2. callback, which is invoked when it checks the file to be an nx romfs or not or in case of errors

It throws

1. TypeError if path is not provided or if provided but not of type String or if callback is not provided or if provided but not of type Function
2. FileNotExists error which specified file does not exists.

Callback has two parameters:

1. First parameter is error which is null in case of success
2. Second parameter is boolean value which indicates if file is nx romfs or not

**Example**

```javascript
var ROMFS_FILE = require("is-nx-romfs-file");

// If a valid nx romfs file is provided and exists at path specified
ROMFS_FILE.isNxRomfs("temp.romfs", function (err, is) {
	if (err) {
		console.log("Error while checking if file is nx romfs: " + err);
	} else {
		console.log("Given file is nx romfs: " + is);
	}
});
//=> Given file is nx romfs: true
```

#### isNxRomfsSync(path)

This is synchronous API for checking if file is an nx romfs. This API takes one parameter:

1. File path which needs to be checked

It throws

1. TypeError if path is not provided or if provided but not of type String
2. FileNotExists error which specified file does not exists.

It returns
Boolean indicating if file at specified path is nx romfs or not

**Example**

```javascript
var ROMFS_FILE = require("is-nx-romfs-file");

// If a valid nx romfs file is provided and exists at path specified
ROMFS_FILE.isNxRomfsSync("temp.romfs");
//=> true
```

### Author

**Migush**

-   [github/Migushthe2nd](https://github.com/Migushthe2nd)

## License

MIT
