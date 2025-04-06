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
1. **User** initiates a task
2. **Application** (program specific to task) receives request
3. **Operating System** interprets the request and directs it to hardware
4. **Hardware** processes the task and sends output back through OS to application
5. Application displays results to user

#### Resource Allocation
- OS handles resource and memory management
- Allocates CPU, memory, storage, and I/O bandwidth
- Balances resources between competing programs
- Task Manager shows resource usage by process

### Common Operating Systems

#### Desktop/Laptop OS
- **Windows**: Introduced 1985, closed-source
- **macOS**: Introduced 1984, partially open-source
- **Linux**: Released 1991, completely open-source

#### Mobile OS
- **Android**: Released 2008, open-source
- **iOS**: Released 2007, partially open-source

#### Other
- **ChromeOS**: Released 2011, partially open-source, popular in education

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

#### Benefits of VMs in Security
- Provides isolated environments (sandboxes)
- Allows secure analysis of malware
- Enables efficient testing across different systems
- Streamlines security tasks

#### Management
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

### Security Analyst Responsibilities
- Configuring and maintaining system security
- Managing access controls
- Analyzing system resources for potential security events
- Investigating and troubleshooting security incidents
- Responding to unusual system behavior
