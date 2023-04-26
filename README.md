# SecurePasswordGenerator
`SecurePasswordGenerator` is a tool for generating random secure passwords. It provides both command line utility (CLI) and underlying python module.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
    - [Command Line Utility](#command-line-utility)
- [License](#license)

## Prerequisites
You'll need to have Python installed in order to run `SecurePasswordGenerator`. Start by downloading and installing [Python](https://www.python.org/downloads/).
> *Note: Python 3 is recommended, however `SecurePasswordGenerator` has been successfully tested with Python 2.6+*


## Installation
```
python -m pip install securepasswordgenerator
```

## Usage
`SecurePasswordGenerator` provides the following methods:
```py
securepasswordgenerator.generate(length = 10, use_lower_case = True, use_upper_case = True, use_numbers = True, use_special = False, use_hex = False)
securepasswordgenerator.decent() 
securepasswordgenerator.strong() 
securepasswordgenerator.fort_knox() 
securepasswordgenerator.ci_key() 
securepasswordgenerator.wep_64() 
securepasswordgenerator.wep_128() 
securepasswordgenerator.wep_152() 
securepasswordgenerator.wep_256() 
securepasswordgenerator.wpa_160() 
securepasswordgenerator.wpa_504()
```

Sample code:
```py
>>> import securepasswordgenerator
>>> securepasswordgenerator.generate()
'ZgnoiVCQ'
>>> securepasswordgenerator.generate(15, use_lower_case=False, use_numbers=False, use_special=True)
'<)G,{IH~NDGZ+D@'
>>> securepasswordgenerator.decent() 
'CONt8xy4Vw'
>>> securepasswordgenerator.strong() 
'm?c$t?WP<y|}vVf'
>>> securepasswordgenerator.fort_knox() 
"'>[&;6L8?->vXiKWh>Uoe<Uo-.x,Zb"
>>> securepasswordgenerator.ci_key() 
'I9MMEnszZO4mKGJayBXe9kKsEGg7JXBs'
>>> securepasswordgenerator.wep_64() 
'866EE'
>>> securepasswordgenerator.wep_128() 
'9EBD3954549FC'
>>> securepasswordgenerator.wep_152() 
'D5CB8A9668F2153D'
>>> securepasswordgenerator.wep_256() 
'E775C1FA7D96CF94DFB19CB9ED534'
>>> securepasswordgenerator.wpa_160() 
'1XkW\\eHu5,ox9I&K`I<R'
>>> securepasswordgenerator.wpa_504()
"AkW~Z9/)d2rf`JWPU}CcUq*`BTsq8%'i+,~BAp2nf@*t!W&~rlpxq(Grh6>$1rj"
```

### Command Line Utility
`SecurePasswordGenerator` includes a command line utility for generating passwords.
```
securepasswordgenerator --help
usage: securepasswordgenerator.py [-h] [-l] [-L] [-u] [-U] [-n] [-N] [-s] [-S] [-x] [-X] [-DP] [-SP] [-FP] [-ci] [-wpa160] [-wpa504]
                         [-wep64] [-wep128] [-wep152] [-wep256]
                         [length]

The Secure Password or Keygen Generator

positional arguments:
  length                Length of password (default is 8 characters)

options:
  -h, --help            show this help message and exit
  -l, --lower-enable    Use lowercase characters
  -L, --lower-disable   Don't use lowercase characters
  -u, --upper-enable    use upper case characters
  -U, --upper-disable   don't use upper case characters
  -n, --number-enable   use number characters
  -N, --number-disable  don't use number characters
  -s, --special-enable  use special characters
  -S, --special-disable
                        don't use special characters
  -x, --hex-enable      use hex characters
  -X, --hex-disable     don't use hex characters
  -DP, --decent         Generate Memorable Passwords - Perfect for securing your computer or mobile device, or somewhere brute
                        force is detectable.
  -SP, --strong         Generate Strong Passwords - Robust enough to keep your web hosting account secure.
  -FP, --fort_knox      Generate Fort Knox Passwords - Secure enough for almost anything, like root or administrator passwords.
  -ci, --ci_key         Generate CodeIgniter Encryption Keys - Can be used for any other 256-bit key requirement.
  -wpa160, --wpa_160    Generate 160-bit WPA Key
  -wpa504, --wpa_504    Generate 504-bit WPA Key
  -wep64, --wep_64      Generate 64-bit WEP Keys
  -wep128, --wep_128    Generate 128-bit WEP Keys
  -wep152, --wep_152    Generate 152-bit WEP Keys
  -wep256, --wep_256    Generate 256-bit WEP Keys
```
> *Note: `-DP`, `--decent`, `-SP`, `--strong`, `-FP`, `--fort_knox`, `-ci`, `--ci_key`, `-wpa160`, `--wpa_160`, `-wpa504`, `--wpa_504`, `-wep64`, `--wep_64`, `-wep128`, `--wep_128`, `-wep152`, `--wep_152`, `-wep256`, `--wep_256` doesn't require any other arguments*


## License

This project is licensed under the MIT License
```
MIT License

Copyright (c) 2023-present Ali Fayaz (Quill) (quillfires)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```