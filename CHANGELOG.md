# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
This project mostly adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html);


# v2.0.0
### Breaking Change
- Removed:
  - Redundant args has been removed
  - Predefined strengths has been compacted under `-p` or `--pass-word-strength` argument
  - Below is the updated version:
```
usage: securepasswordgenerator [-h] [-l] [-u] [-n] [-s] [-x] [-p {decent,strong,fort_knox,wpa_160,wpa_504,wep_64,wep_128,wep_152,wep_256}] [length]

positional arguments:
  length                Length of password (default is 8 characters)

optional arguments:
  -h, --help            show this help message and exit
  -l, --lower-case      Use lowercase characters
  -u, --upper-case      Use uppercase characters
  -n, --numbers         Use numbers
  -s, --special         Use special characters
  -x, --hex             Use hex characters
  -p {decent,strong,fort_knox,wpa_160,wpa_504,wep_64,wep_128,wep_152,wep_256}, --password-strength {decent,strong,fort_knox,wpa_160,wpa_504,wep_64,wep_128,wep_152,wep_256}
                        Generate a password with a predefined strength
```
### Internal
- generates a password that is 8 characters long that includes atleast 1 lowercase, 1 uppercase, 1 number and 1 special character by default.
- optimized for performance.
- maximum length has been set to 1000 characters.