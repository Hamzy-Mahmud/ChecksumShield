# File Integrity Checker

Sample solution for the [file-integrity-checker](https://roadmap.sh/projects/file-integrity-checker) challenge from [roadmap](https://roadmap.sh)

## Prerequisites

- Linux operating system with installed `git`
- sha256

## Installation

**Clone the Repository**

- Clone this repository into the local machine.

```bash
git clone --depth=1 https://github.com/Aj-Seven/DevOps-Projects.git

cd DevOps-Projects/file-integrity-checker
chmod +x integrity-check
```

- Example Usage:
```sh
> ./integrity-check init /var/log  # Initializes and stores hashes of all log files in the directory
> ./integrity-check init hello.txt
> Hashes stored successfully.

> ./integrity-check check /var/log/syslog
> Status: Modified (Hash mismatch)
# Optionally report the files where hashes mismatched

> ./integrity-check -check /var/log/auth.log
> Status: Unmodified

> ./integrity-check update /var/log/syslog
> Hash updated successfully.
```

**Note:**
> Hash files are stored in base path - `~/.local/share/hash`
>
> Hash File Format's - `filename-date.sha256sum` or `pathname-date.sha256sum`
>
> Date Format - +%Y-%m-%d_%H-%M-%S
