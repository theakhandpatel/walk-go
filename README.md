# Walk-Go

Walk-Go is a filesystem crawler written in Go. It allows you to traverse a directory tree and perform actions on the files based on certain criteria.

## Features

- File Listing: List all files in a directory tree.
- File Deletion: Delete files based on certain criteria.
- File Filtering: Filter files based on their extension and size.
- Logging: Log deleted files to a specified log file.

## Usage

You can use Walk-Go by running the `main.go` file with the following command-line flags:

- `-root`: The root directory to start the traversal. Default is the current directory.
- `-list`: If set, the program will only list the files.
- `-del`: If set, the program will delete the files that match the criteria.
- `-ext`: The file extension to filter out.
- `-size`: The minimum file size to consider.
- `-log`: The file to log deleted files to.

Here is an example of how to use Walk-Go:

```bash
go run main.go -root ./mydir -list -ext .txt -size 100 -log deletelog.txt
```

This command will list all `.txt` files in the `mydir` directory that are at least 100 bytes in size and log the deleted files to `deletelog.txt`. If the `-del` flag is set instead of `-list`, the files will be deleted.

## Testing
Tests for Walk-Go are located in main_test.go and actions_test.go. You can run the tests for Walk-Go by running the following command:

```bash
go test
```

## Contributing
Contributions are welcome! If you have any ideas or suggestions, feel free to open an issue or a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
```