## Installation

This method of installation uses creates a virtual environment, installs requires modules and packges, then clones the git repository.

### Requirements

- Python is required and can be downloaded at - https://www.python.org/
- GitHub account - https://github.com
- Git - https://git-scm.com/

### Installing Git
> Git is required to clone the repository from GitHub

Git can be installed with 'winget' which is usually installed by default in Windows.
```sh
winget install --id Git.Git -e --source winget
```
If 'winget' is not installed, it can be installed from the Microsoft Store.

### Setting up script for Windows
> Example here uses PowerShell

Install 'virtualenv' module
```sh
pip install virtualenv
```
Create folder to store virtual environments
```sh
cd ~
mkdir .venvs
```
Create and activate virutal environment
```sh
cd .venvs
python -m virtualenv pingsweep --prompt pingsweep
cd .\pingsweep\Scripts
.\activate
```
Clone git repository
```sh
cd ~
mkdir python_projects #optionally you can create a folder to store project
cd python_projects
git clone git@github.com:jzmack/pingsweep.git
```
### Setting up script for Linux/Mac
> Example here is for a Debian based system.

Install required apt packages for virtual environment
```sh
sudo apt update
sudo apt install python3-pip
sudo apt install python3-virtualenv
```
Create a folder to store virtual environments
```sh
cd ~
mkdir .venvs
cd .venvs
```
Create virtual environment
```sh
python3 -m virtualenv pingsweep --prompt pingsweep
source /pingsweep/bin/activate
```
Install the required dependencies in virtual environment:
```sh
pip install -r requirements.txt
```
Clone the repository into the virtual environment
```sh
git clone git@github.com:jzmack/pingsweep.git
cd pingsweep
```

## Usage

Running the script:
```sh
python pingsweep.py
```
Run to show available arguments:
```sh
python pingsweep.py -h
```
Run the script with the desired subnet in CIDR notation:
```sh
python pingsweep.py -s 192.168.1.0/24
```
You can also specify the timeout and the number (count) of packets to send:
```sh
python pingsweep.py -s 192.168.1.0/24 -t 0.5 -c 3
```
## License

This project is licensed under the MIT License - see the LICENSE file for details.

Feel free to customize the `README.md` file to better suit your project's needs. If you have any more questions or need further assistance, let me know!