# ScanQLi [![License](https://img.shields.io/badge/license-GPLv3-red.svg)](https://github.com/bambish/ScanQLi/LICENSE.md) ![Python 2|3](https://img.shields.io/badge/python-2|3-yellow.svg) [![Twitter](https://img.shields.io/badge/twitter-@bambishee-blue.svg)](https://twitter.com/bambishee)

![Screenshot](https://github.com/bambish/ScanQLi/.screenshots/scanqli.jpg)

ScanQLi is a simple SQL injection scanner with somes additionals features like recurise scan or cookies integration. This tool can detect severals types of SQLi:
* Classic
* Blind
* Time based
* _GBK (soon)_

Tested with:
* Debian 9
* Python 2.7
* Python 3.5

### Prerequisites
----

**1.** Install git tool
```
apt update
apt install git
```

**2.** Clone the repo.
```
git clone https://github.com/bambish/ScanQLi
```

**3.** Install python required libs
```
apt install python-pip
cd ScanQLi
pip install -r requirements.txt
```
_For python3 please install **python3-pip** and use **pip3**_

### Usage
----

```
./scanqli -u [URL] [OPTIONS]
```

### Examples
----

Simple url scan with output file
```
python scanqli.py -u 'http://127.0.0.1/test/?p=news' -o output.log
```

Recursive URL scanning with cookies
```
python scanqli.py -u 'https://127.0.0.1/test/' -r -c '{"PHPSESSID":"4bn7uro8qq62ol4o667bejbqo3" , "Session":"Mzo6YWMwZGRmOWU2NWQ1N2I2YTU2YjI0NTMzODZjZDVkYjU="}'
```