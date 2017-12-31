##urlscan-py

## Description:

Urlscan-py is a Python wrapper for urlscan.io's API to scan URLs.


## Requirements:

- Python3


## Installation and Usage:

Edit the urlscan_api variable in urlscan to equal a valid urlscan.io API key.


#### Scanning:

`./urlscan scan --url https://google.com`

The resulting output will produce a UUID. The UUID will be needed in order to retrieve the scan results. The output will also indicate whether the scan was successfully started or not.

The `--url` flag can accept more than one URL at a time.


```
./urlscan scan --help

usage: urlscan scan [-h] --url URL [URL ...] [-q]

optional arguments:
  -h, --help           show this help message and exit
  --url URL [URL ...]  URL(s) to scan
  -q, --quiet          suppress output
```


#### Retrieve the scan results:

`./urlscan retrieve --uuid UUID`

This will print the scan with the associated UUID to STDOUT. The `--uuid` flag can accept more than one UUID at a time.

#### Save retrieved results to directory:

`./urlscan retrieve --uuid UUID --dir DIRECTORY`

```
./urlscan retrieve --help

usage: urlscan retrieve [-h] --uuid UUID [UUID ...] [-s] [-d DIRECTORY] [-q]

optional arguments:
  -h, --help            show this help message and exit
  --uuid UUID [UUID ...]
                        UUID(s) to retrieve scans for
  -s, --save            save UUID with a timestamp to index file for future
                        reference
  -d, --dir DIRECTORY
                        directory to save scans to
  -q, --quiet           suppress output
```


## To do:

1.  Add functionality to sort/filter through retrieved scans.
