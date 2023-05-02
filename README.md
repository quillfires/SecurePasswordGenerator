This is a tool for generating random secure passwords. It provides both command line utility (CLI) and underlying python module.

# SecurePasswordGenerator
[![Python Version](https://img.shields.io/badge/Python-3.7%20%7C%203.8%20%7C%203.9%20%7C%203.10%20%7C%203.11-blue.svg)](https://www.python.org)  [![securepasswordgenerator · PyPI](https://img.shields.io/pypi/v/securepasswordgenerator.svg?color=4CBB17)](https://pypi.org/project/securepasswordgenerator/)  [![PyPI - Status](https://img.shields.io/pypi/status/securepasswordgenerator)](https://pypi.org/project/securepasswordgenerator/)  [![Maintenance](https://img.shields.io/maintenance/yes/2030)](https://pypi.org/project/securepasswordgenerator/)  [![LICENSE](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/quillfires/SecurePasswordGenerator/blob/main/LICENSE)

[![ViewCount](https://views.whatilearened.today/views/github/quillfires/SecurePasswordGenerator.svg)](https://views.whatilearened.today/views/github/quillfires/SecurePasswordGenerator.svg)  [![GitHub forks](https://img.shields.io/github/forks/quillfires/SecurePasswordGenerator)](https://github.com/quillfires/SecurePasswordGenerator/forks)  [![GitHub stars](https://img.shields.io/github/stars/quillfires/SecurePasswordGenerator.svg?color=ffd40c)](https://github.com/quillfires/SecurePasswordGenerator/stargazers)  [![PyPI - Downloads](https://img.shields.io/pypi/dm/securepasswordgenerator?color=orange&label=PIP%20-%20Installs)](https://pypi.org/project/securepasswordgenerator/) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/quillfires/SecurePasswordGenerator/issues)  [![GitHub issues](https://img.shields.io/github/issues/quillfires/SecurePasswordGenerator.svg?color=808080)](https://github.com/quillfires/SecurePasswordGenerator/issues)  


## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
    - [Python Module](#module)
    - [Command Line Utility](#command-line-utility)
- [License](#license)


## Prerequisites
You'll need to have Python installed in order to run `SecurePasswordGenerator`. Start by downloading and installing [Python](https://www.python.org/downloads/).
> *Note: Python 3 is recommended, however `SecurePasswordGenerator` has been successfully tested with Python 2.6+*


## Installation
You can install this package from PyPI using pip:
```
python -m pip install securepasswordgenerator
```


## Usage
### Module
To use this package in your Python program, simply import the `securepasswordgenerator` module and call the `generate` function with the desired options. Or call predefined functions. Here is an example:
```python
from securepasswordgenerator.password import generate

password = generate(length=12, use_lower_case=True, use_upper_case=True, use_numbers=True, use_special=True, use_hex=False)
```
This will generate a password that is 12 characters long and includes lowercase letters, uppercase letters, numbers, and special characters.

`securepasswordgenerator` provides the following methods:
```python
securepasswordgenerator.generate()
# defaults to 8 characters long that includes atleast 1 lowercase, 1 uppercase, 1 number and 1 special character.
securepasswordgenerator.generate(length = 8, use_lower_case = True, use_upper_case = True, use_numbers = True, use_special = True, use_hex = False)
# optins can be provided to generate as you please.
securepasswordgenerator.decent() 
# Generate Memorable Passwords - Perfect for securing your computer or mobile device, or somewhere brute force is detectable.
securepasswordgenerator.strong() 
# Generate Strong Passwords - Robust enough to keep your web hosting account secure.
securepasswordgenerator.fort_knox() 
# Generate Fort Knox Passwords - Secure enough for almost anything, like root or administrator passwords.
securepasswordgenerator.ci_key() 
# Generate CodeIgniter Encryption Keys - Can be used for any other 256-bit key requirement.
securepasswordgenerator.wep_64() 
# Generate 64-bit WEP Keys
securepasswordgenerator.wep_128() 
# Generate 128-bit WEP Keys
securepasswordgenerator.wep_152() 
# Generate 152-bit WEP Keys
securepasswordgenerator.wep_256() 
# Generate 256-bit WEP Keys
securepasswordgenerator.wpa_160() 
# Generate 160-bit WPA Key
securepasswordgenerator.wpa_504()
# Generate 504-bit WPA Key
```

Sample code:
```python
>>> import securepasswordgenerator as spw
>>> spw.generate()
'ZgnoiV*Q'
>>> spw.generate(15, use_lower_case=False, use_numbers=False, use_special=True)
'<)G,{IH~NDGZ+D@'
>>> spw.decent() 
'CONt8xy4Vw'
>>> spw.strong() 
'm?c$t?WP<y|}vVf'
>>> spw.fort_knox() 
"'>[&;6L8?->vXiKWh>Uoe<Uo-.x,Zb"
>>> spw.ci_key() 
'I9MMEnszZO4mKGJayBXe9kKsEGg7JXBs'
>>> spw.wep_64() 
'866EE'
>>> spw.wep_128() 
'9EBD3954549FC'
>>> spw.wep_152() 
'D5CB8A9668F2153D'
>>> spw.wep_256() 
'E775C1FA7D96CF94DFB19CB9ED534'
>>> spw.wpa_160() 
'1XkW\\eHu5,ox9I&K`I<R'
>>> spw.wpa_504()
"AkW~Z9/)d2rf`JWPU}CcUq*`BTsq8%'i+,~BAp2nf@*t!W&~rlpxq(Grh6>$1rj"
```

### Command Line Utility
To generate a password from the command line, simply run the `securepasswordgenerator` command and specify the desired options. Here are a few examples:

```
securepasswordgenerator
```
This will generate a password that is 8 characters long that includes atleast 1 lowercase, 1 uppercase, 1 number and 1 special character.

```
securepasswordgenerator 11 -l -n -s -x -p
```
This will generate a password that is 15 characters long and includes lowercase letters, numbers, special characters, and hex characters.

Here are the available options:
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
> *Note: `securepasswordgenerator -p [option]` or `securepasswordgenerator --password-strength [option]` doesn't require any other arguments*


# Changlog
[See the change log here](https://github.com/quillfires/SecurePasswordGenerator/blob/main/CHANGELOG.md)


## License

This package is licensed under the MIT License. See the [LICENSE](https://github.com/quillfires/SecurePasswordGenerator/blob/main/LICENSE) file for details.