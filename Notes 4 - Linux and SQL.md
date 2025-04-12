# Course 4: Tools of the Trade - Linux and SQL

## Module 1: Introduction to Operating Systems

### Core Concepts

#### What is an Operating System?
- Interface between computer hardware and users
- Manages computer resources efficiently
- Bridges communication between humans and computers (which use binary)
- Makes computers usable by running multiple applications simultaneously
- Provides access to external devices (printers, keyboards, etc.)

#### OS Boot Process
1. Power button activates hardware
2. BIOS/UEFI microchip activates
   - BIOS (Basic Input/Output System) - older systems
   - UEFI (Unified Extensible Firmware Interface) - modern systems with enhanced security features
3. BIOS/UEFI verifies hardware health and activates the bootloader
4. Bootloader starts the operating system

#### How OS Works: Task Completion Process
1. User initiates a task
2. Application (program specific to task) receives request
3. Operating System interprets the request and directs it to hardware
4. Hardware processes the task and sends output back through OS to application
5. Application displays results to user

#### Resource Allocation
- OS handles resource and memory management
- Allocates CPU, memory, storage, and I/O bandwidth
- Balances resources between competing programs
- Task Manager shows resource usage by process

### Common Operating Systems

#### Desktop/Laptop OS
- Windows: Introduced 1985, closed-source
- macOS: Introduced 1984, partially open-source
- Linux: Released 1991, completely open-source

#### Mobile OS
- Android: Released 2008, open-source
- iOS: Released 2007, partially open-source

#### Other
- ChromeOS: Released 2011, partially open-source, popular in education

### User Interfaces

#### Graphical User Interface (GUI)
- Uses icons, windows, and menus
- Visual approach to operating a computer
- Components: start menu, taskbar, desktop with icons/shortcuts
- Easier for beginners but limited to one task at a time
- Less efficient for multiple repetitive tasks

#### Command-Line Interface (CLI)
- Text-based interface using typed commands
- More flexible and powerful than GUI
- Advantages for security professionals:
  - Allows multiple simultaneous tasks
  - More efficient for repetitive tasks (e.g., batch operations)
  - Records history file of all commands (useful for incident response)
  - Provides better traceability of actions

### Virtualization

#### Virtual Machines (VMs)
- Software-based version of a physical computer
- Uses virtualized hardware rather than physical components
- Multiple VMs can share resources of a single physical host
- Benefits of VMs in Security:
  - Provides isolated environments (sandboxes)
  - Allows secure analysis of malware
  - Enables efficient testing across different systems
  - Streamlines security tasks
- Management:
  - Hypervisors (like KVM) manage VMs and allocate resources
  - Virtual servers and networks can be created from physical hardware

### Security Considerations

#### OS Security Fundamentals
- Securing files, data access, and user authentication
- Managing and configuring firewalls
- Setting security policies
- Enabling virus protection
- Performing auditing, accounting, and logging

#### Legacy OS Risks
- Outdated systems still in use are vulnerable
- Often lack security updates
- Common in industries using embedded software

#### Vulnerabilities
- All operating systems have security issues
- Keeping systems updated is crucial
- Resources for vulnerability tracking:
  - Microsoft Security Response Center
  - Apple Security Updates
  - Common Vulnerabilities and Exposures (CVE) Report
  - Google Cloud Security Bulletin

#### Security Analyst Responsibilities
- Configuring and maintaining system security
- Managing access controls
- Analyzing system resources for potential security events
- Investigating and troubleshooting security incidents
- Responding to unusual system behavior

## Module 2: The Linux Operating System

### Introduction to Linux

#### Definition and Origin
- Linux is an open-source operating system widely used in cybersecurity
- Created through the combination of:
  - Linus Torvalds' Linux kernel
  - Richard Stallman's GNU operating system

#### Key Features
- Open source (free to use, modify, and share)
- Strong community development support
- Multiple distributions (600+) for different purposes
- Commonly used in security tools and programs

#### Security Applications
- Log examination and analysis
- Identity and access management
- Digital forensics
- Penetration testing

### Linux Architecture

The Linux architecture consists of six main components that work together:

1. **User**: The person interacting with the computer (Linux supports multiple simultaneous users)

2. **Applications**: Programs that perform specific tasks
   - Installed via package managers
   - Packages can be combined to form applications

3. **Shell**: Command-line interpreter that processes commands and outputs results
   - Allows users to communicate with the OS
   - Translates user commands for the kernel
   - Multiple shell types exist (bash, csh, ksh, etc.)
   - Bash is the most common in cybersecurity

4. **Filesystem Hierarchy Standard (FHS)**: Organizes data storage
   - Specifies file/directory locations in the OS
   - Directories contain files or other directories

5. **Kernel**: Manages processes and memory
   - Communicates with hardware to execute commands
   - Uses drivers to enable application execution
   - Helps allocate system resources efficiently

6. **Hardware**: Physical components of the computer
   - Peripheral devices: External components (monitor, keyboard, mouse)
   - Internal hardware: Core components
     - CPU (Central Processing Unit): Main processor
     - RAM (Random Access Memory): Short-term memory
     - Hard drive: Long-term storage

### Linux Distributions

Distribution (distro): Different versions of Linux with specific tools, interfaces, and purposes

#### Major Parent Distributions
- Debian (parent to Ubuntu, KALI LINUX, Parrot)
- Red Hat (parent to CentOS)
- Slackware (parent to SUSE)

#### Security-Focused Distributions

##### KALI LINUX
- Debian-derived, focused on penetration testing and digital forensics
- Pre-installed security tools:
  - Metasploit: Vulnerability exploitation
  - Burp Suite: Web application testing
  - John the Ripper: Password cracking
  - tcpdump: Packet analysis
  - Wireshark: Network traffic analysis
  - Autopsy: Hard drive and smartphone forensics
- Best used on virtual machines for safety

##### Parrot
- Debian-based with pre-installed security tools
- User-friendly with both GUI and CLI

##### Ubuntu
- User-friendly Debian-derived distribution
- Widely used in security and cloud computing
- Has both CLI and GUI interfaces
- Large community support

##### Red Hat Enterprise Linux
- Subscription-based for enterprise use
- Dedicated customer support

##### AlmaLinux
- Community-driven replacement for CentOS
- Compatible with applications designed for CentOS

### Package Management

#### Package
- Software piece that can be combined with others to form an application
- Contains files and dependencies needed for installation

#### Package Managers
- Tools that help install, manage, and remove packages
- Different managers for different distributions
- Important for keeping software updated with security patches

#### Common Package Managers
- For Debian-based distributions (Ubuntu, KALI LINUX, Parrot):
  - dpkg (.deb file extension)
  - APT (Advanced Package Tool) - command-line tool
- For Red Hat-based distributions:
  - RPM (Red Hat Package Manager) (.rpm file extension)
  - YUM (Yellowdog Updater Modified) - command-line tool

### The Shell

#### Purpose
- Interface between user and operating system
- Allows communication through commands
- Executes applications
- Automates tasks

#### Common Shell Types
- Bash (Bourne-Again Shell) - default in most Linux distributions
- C Shell (csh)
- Korn Shell (ksh)
- Enhanced C shell (tcsh)
- Z Shell (zsh)

#### Shell Communication Process
- Standard Input: Information received via command line (keyboard)
- Standard Output: Information returned by the OS (display)
- Standard Error: Error messages returned by the OS

### Key Cybersecurity Applications

#### Penetration Testing
- Simulated attacks to identify vulnerabilities
- Uses tools like Metasploit, Burp Suite

#### Digital Forensics
- Collecting and analyzing data after an attack
- Uses tools like tcpdump, Wireshark, Autopsy

### Career Advice for Cybersecurity
- Always continue learning as technology constantly evolves
- Don't get overwhelmed; learn incrementally
- Focus on building a foundation of knowledge
- Start with small coding projects, then expand skills
- Reference materials when needed; no one memorizes everything

## Module 3: Command Line & Linux File System

### Linux File System Hierarchy

#### Filesystem Hierarchy Standard (FHS)
- Organizes data in Linux in a hierarchical structure
- Root Directory: Highest-level directory, represented by a single forward slash (/)
- File Path: Location of a file/directory with levels separated by forward slashes

#### Standard FHS Directories
- `/home`: Contains user home directories
- `/bin`: Contains binary executables
- `/etc`: Stores system configuration files
- `/tmp`: Stores temporary files (security note: common target for attackers)
- `/mnt`: Mount point for external media

#### Path Notation
- Absolute Path: Full path starting from root (e.g., /home/analyst/logs)
- Relative Path: Path relative to current location
- Special Notations: ~ (user's home directory), . (current directory), .. (parent directory)

### Navigation & Reading Files

#### Navigation Commands
- `pwd`: Print working directory (shows current location)
- `ls`: List files and directories in current location
- `cd`: Change directory
  - `cd directory` - move to specified directory
  - `cd ..` - move up one level
  - `cd ~` - move to home directory

#### Reading File Content
- `cat [filename]`: Display entire file content
- `head [filename]`: Display first 10 lines of a file (use -n to specify number of lines)
- `tail [filename]`: Display last 10 lines of a file
- `less [filename]`: View file content one page at a time
  - Navigation: Space (forward), b (back), arrows (line by line), q (quit)

### Filtering & Finding Content

#### grep Command
- `grep [pattern] [file]`: Search for specific pattern in a file
- Returns all lines containing the specified pattern
- Case-sensitive by default

#### Piping
- Uses the pipe character (|) to send output from one command as input to another
- Example: `ls /home/analyst/reports | grep users` lists only files/directories containing "users"

#### find Command
- Searches for files and directories based on specific criteria
- Basic syntax: `find [starting directory] [options]`
- Useful options:
  - `-name "pattern"`: Case-sensitive search for files with matching name
  - `-iname "pattern"`: Case-insensitive search for files with matching name
  - `-mtime n`: Files modified n days ago
  - `-mtime +n`: Files modified more than n days ago
  - `-mtime -n`: Files modified less than n days ago
  - `-mmin n`: Similar to mtime but works with minutes

### File & Directory Management

#### Creating & Removing Directories
- `mkdir [directory]`: Create new directory
- `rmdir [directory]`: Remove empty directory

#### Creating & Managing Files
- `touch [filename]`: Create new empty file
- `rm [filename]`: Remove/delete a file
- `mv [source] [destination]`: Move file/directory to new location
- `mv [filename] [new_filename]`: Rename a file
- `cp [source] [destination]`: Copy file/directory to new location

#### File Editing
- `nano [filename]`: Open/create file in nano text editor
  - Save: Ctrl+O, then Enter
  - Exit: Ctrl+X
- Other editors: vim, emacs (more advanced)

#### Output Redirection
- `>`: Redirect output to a file (overwrites existing content)
- `>>`: Append output to the end of a file
- Example: `echo "text" > file.txt` writes "text" to file.txt (overwrites)
- Example: `echo "more text" >> file.txt` appends "more text" to file.txt

### File Permissions & Ownership

#### Understanding Permissions
- Permissions in Linux determine what actions users can perform on files and directories
- Three types of permissions:
  - Read (r): View file contents or list directory contents
  - Write (w): Modify file contents or create/delete files in a directory
  - Execute (x): Run a file as a program or access files within a directory

#### Permission Categories
- Permissions are granted to three owner types:
  - User (u): The owner of the file
  - Group (g): Users who belong to the file's group
  - Other (o): All other users on the system

#### Reading Permission Strings
- Linux represents permissions with a 10-character string:
  - 1st character: File type (d for directory, - for regular file)
  - 2nd-4th characters: User permissions (rwx)
  - 5th-7th characters: Group permissions (rwx)
  - 8th-10th characters: Other permissions (rwx)
- Example: -rw-r--r--
  - Regular file (-)
  - User can read and write (rw-)
  - Group can only read (r--)
  - Other can only read (r--)

#### Checking Permissions
- `ls -l`: List files with permissions information
- `ls -a`: Show hidden files (those starting with .)
- `ls -la`: Combine both options (show hidden files with permissions)

#### Changing Permissions
- The `chmod` command changes permissions on files/directories:
- Syntax: `chmod [who][operation][permissions] filename`
  - who: u (user), g (group), o (other), or a (all)
  - operation: + (add), - (remove), = (set exactly)
  - permissions: r (read), w (write), x (execute)
- Examples:
  - `chmod g+w,o-r access.txt`: Add write permission for group, remove read for others
  - `chmod u=rw,g=r,o= file.txt`: Set user to read+write, group to read-only, others to no access

### User Management

#### User Authentication & Authorization
- Authentication: Verifying who someone is
- Authorization: Determining what resources they can access

#### Root User & Sudo
- Root user: Has complete system access (superuser)
- Problems with using root: Security risks, irreversible mistakes, lack of accountability
- sudo: Grants temporary elevated permissions to specific users
  - Comes from "superuser do"
  - Requires user to be in the sudoers file
  - Preferred over logging in as root

#### User Management Commands

| Command | Description | Example |
|---------|-------------|---------|
| useradd | Add a new user | sudo useradd username |
| userdel | Delete a user | sudo userdel username |
| usermod | Modify user account | sudo usermod -option username |
| chown | Change file owner | sudo chown user:group file |

#### Common Options
- useradd -g: Set primary group
- useradd -G: Add to supplemental groups
- usermod -a -G: Add to supplemental group without replacing existing groups
- usermod -d: Change home directory
- usermod -L: Lock account
- userdel -r: Delete user and their home directory
- chown user:group file: Change both user and group ownership

#### Principle of Least Privilege
- Grant users only the minimum access required to perform their job
- World-writable files (accessible by all users) pose significant security risks
- Regularly review and update permissions when users change roles or leave

### Linux Support Resources

#### Command Line Help
- `man [command]`: Display manual pages for commands
- `whatis [command]`: Show brief description of a command
- `apropos [keyword]`: Search manual pages for relevant commands
- `apropos -a [word1] [word2]`: Search for commands containing both words

#### External Resources
- Linux has a large global community of users
- Unix & Linux Stack Exchange: Community Q&A with ranked answers
- Online searches often provide solutions to common problems

### Best Practices
- Use absolute paths when unsure of your current location
- Always verify operations with commands like ls after creating/removing content
- Be cautious with rm and > as they can permanently delete content
- Organization is crucial for security operations - maintain a logical directory structure

## Module 4: SQL

### Introduction to Databases

#### Database Fundamentals
- Database: An organized collection of information or data
- Relational database: A structured database containing tables that are related to each other
- Advantages over spreadsheets: Multiple simultaneous users, massive data storage, complex operations

#### Table Structure
- Tables: Collections of related data in rows and columns
- Columns/Fields: Categories of information (e.g., employee_id, username)
- Rows/Records: Individual entries containing data for each column

#### Keys in Databases
- Primary key: A column with unique entries for each row (no duplicates or nulls)
  - Uniquely identifies each record in a table
  - A table can have only one primary key
- Foreign key: A column that is a primary key in another table
  - Can contain duplicates and null values
  - Used to establish relationships between tables
  - A table can have multiple foreign keys

### SQL Basics

#### Introduction to SQL
- SQL (Structured Query Language): Programming language used to create, interact with, and request information from databases
- Query: A request for data from a database table or combination of tables

#### Basic SQL Query Structure
- SELECT: Indicates which columns to return
- FROM: Indicates which table to query
- Basic syntax: `SELECT column FROM table;`
- **SELECT ***: Returns all columns from a table

#### Syntax Rules
- SQL keywords are not case-sensitive (conventionally written in UPPERCASE)
- Statements end with semicolons
- Table and column references are case-sensitive in some SQL implementations

#### Data Types in SQL
- String data: Ordered sequence of characters (letters, numbers, symbols)
  - Example: Usernames, names
- Numeric data: Numbers that can be used in mathematical operations
  - Example: Login attempt counts
- Date and time data: Data representing dates and/or times
  - Example: Login timestamps, patch dates

### SQL Filters

#### Basic Filtering
- WHERE clause: Indicates condition for filtering
- Basic syntax: `SELECT column FROM table WHERE condition;`

#### String Filters
- Equal operator: `WHERE column = 'value'`
- Pattern matching with LIKE operator and wildcards:
  - % wildcard: Represents any number of characters
  - _ wildcard: Represents exactly one character
- Examples:
  - 'a%' matches values starting with 'a'
  - 'a_' matches two-character values starting with 'a'
  - '%a%' matches values containing 'a' anywhere

#### Numeric and Date Filters
- Comparison operators:
  - Less than: <
  - Greater than: >
  - Equal to: =
  - Less than or equal to: <=
  - Greater than or equal to: >=
  - Not equal to: <> or !=
- BETWEEN operator: Filters for values within a range (inclusive)
  - Example: `WHERE date BETWEEN '2021-01-01' AND '2021-12-31'`

#### Multiple Conditions
- AND operator: Both conditions must be true
  - Example: `WHERE os = 'OS 1' AND email_client = 'Email Client 1'`
- OR operator: Either condition can be true
  - Example: `WHERE os = 'OS 1' OR os = 'OS 3'`
- NOT operator: Negates a condition
  - Example: `WHERE NOT os = 'OS 3'`

#### Formatting Notes
- String, date, and time values require quotation marks
- Numeric values do not use quotation marks

#### Organizing Results
- ORDER BY: Sequences records based on specified column(s)
  - Default: Ascending order (ASC)
  - Descending order: Add DESC keyword
  - Multiple columns: `ORDER BY country, city`
- Example: `SELECT name FROM users ORDER BY login_date DESC;`

### Joining Tables

#### Join Basics
- Joins combine data from multiple tables based on related columns
- Column reference format when using multiple tables: table_name.column_name

#### Types of Joins

##### INNER JOIN
- Returns only rows with matching values in the specified columns
- Syntax:
```sql
SELECT columns
FROM table1
INNER JOIN table2 ON table1.column = table2.column;
```

##### LEFT JOIN
- Returns all rows from the left (first) table and matching rows from the right table
- Non-matching rows from right table contain NULL values
- Syntax:
```sql
SELECT columns
FROM table1
LEFT JOIN table2 ON table1.column = table2.column;
```

##### RIGHT JOIN
- Returns all rows from the right (second) table and matching rows from the left table
- Non-matching rows from left table contain NULL values
- Syntax:
```sql
SELECT columns
FROM table1
RIGHT JOIN table2 ON table1.column = table2.column;
```

##### FULL OUTER JOIN
- Returns all rows from both tables
- Non-matching values from either table contain NULL values
- Syntax:
```sql
SELECT columns
FROM table1
FULL OUTER JOIN table2 ON table1.column = table2.column;
```

#### Aggregate Functions
- Functions that perform calculations over multiple rows
- Common aggregate functions:
  - COUNT: Returns the number of rows
  - AVG: Returns the average of numeric values
  - SUM: Returns the sum of numeric values
- Basic syntax: `SELECT COUNT(column) FROM table;`

### Practical Cybersecurity Applications

#### Security Logs Analysis
- Reviewing login attempts (time, location, success/failure)
- Identifying machines without required patches
- Finding configuration issues across systems

#### Vulnerability Management
- Identifying machines with specific combinations of software
- Finding systems requiring updates
- Determining optimal update times based on usage patterns

#### Data-Driven Decision Making
- Using SQL to extract specific security data to support decisions
- Analyzing patterns and anomalies in security logs
- Providing evidence for security recommendations

#### SQL vs. Linux Filtering
- SQL works with structured database data; Linux works with files and directories
- SQL provides better structure and readability for data analysis
- SQL allows table joining; Linux does not
- Some logs are only accessible through Linux filtering (not in database format)

### Best Practices
- Create targeted queries that return only needed data
- Use appropriate joins to combine related information
- Add filters to narrow results to relevant records
- Use meaningful table and column references when working with multiple tables
