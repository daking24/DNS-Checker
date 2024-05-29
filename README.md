# DNS Record Checker

## Description
This is a simple Go program that checks DNS records for a given domain. It reads input from the standard input, checks the domain for various DNS records, and then prints out the results in a CSV-like format.

## Features
- Checks for MX records
- Checks for SPF records
- Checks for DMARC records

## Requirements
- Go (version 1.16 or higher)

## Installation
1. Clone the repository.
2. Run the program using `go run main.go`.

## Usage
To use the program, simply run it and enter the domain names you want to check, one per line. The program will print out the results in a CSV-like format.

## Example
```sh
$ go run main.go
domain,hasMX,hasSPF,sprRecord,hasDMARC,dmarcRecord
example.com,true,true,"v=spf1 mx a ip4:192.0.2.0/24 -all",true,"v=DMARC1; p=none; sp=none; rua=mailto:postmaster@example.com; ruf=mailto:postmaster@example.com; pct=100"
example.org,false,false,"",false,""
example.net,true,true,"v=spf1 mx a ip4:192.0.2.0/24 -all",true,"v=DMARC1; p=none; sp=none; rua=mailto:postmaster@example.net; ruf=mailto:postmaster@example.net; pct=100"
```

## Error Handling
The program handles errors that may occur during the DNS lookup process. If an error occurs, it will be logged to the console.

## License
This program is licensed under the MIT License.

## Contact
If you have any questions or comments, please contact the author at [kingdavidao@gmail.com](mailto:kingdavidao@gmail.com).