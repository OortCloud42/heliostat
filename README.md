# heliostat

This Bash script updates the Arch Linux mirrorlist by fetching and ranking mirrors from archlinux.org/mirrorlist.

## Features

- Specify preferred / trusted countries and the number of top mirrors to use
- Rank mirrors based on speed
- Replace the current mirrorlist or dump to stdout without modifying the existing one.

## Prerequisites

- `bash`
- `curl`
- `rankmirrors` (from `pacman-contrib`)

## Usage

```bash
./heliostat [-c <country_list>] [-n <num_mirrors>] [-r] [-h] [-v]
```

- `-c <country_list>`: Comma-separated list of countries (default: all)
- `-n <num_mirrors>`: Number of mirrors to use (default: 5)
- `-r`: Replace the current mirrorlist (default: false)
- `-f`: Skip confirmation before replacing mirrorlist (default: false)
- `-v`: Verbose mode (default: false)
- `-h`: Show help message

Example:
```bash
./heliostat -c US,CA -n 10 -r
```
