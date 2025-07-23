# DevOps Theory

## 1. What is SDLC?

**Software Development Life Cycle (SDLC)** is the end‑to‑end process development teams follow to design, build, test, and deploy software systems.  
In a DevOps context, SDLC is commonly viewed in **two major parts**:

---

#### A. Software Development – handled by the Development Team

- **(a) Requirements Gathering :** Understand business/user needs. Define project goals and features.  
- **(b) Designing & Planning :** Create architecture, workflows, and UI/UX design. Decide technologies and system components.  
- **(c) Testing / Code Development :** Developers write source code based on the design; version control is used (e.g., Git).  
- **(d) Testing (Unit / Integration) :** Basic testing to ensure code works as expected; unit and integration tests run during development.  

---

#### B. Operations – handled by the Operations / DevOps Team

- **(e) Build :** Code is compiled, dependencies resolved, and an application package is produced. Automated build tools (e.g., Jenkins, Maven).  
- **(f) Infrastructure Provisioning :** Set up servers, databases, networks via Infrastructure as Code (IaC). Tools: Terraform, Ansible.  
- **(g) Deployment :** Deploy the application to staging or production. Strategies: Blue‑Green, Rolling, Canary deployments.  
- **(h) Monitoring & Feedback :** Monitor system/application health (CPU, errors, logs). Tools: Prometheus, Grafana, ELK Stack.  

## 2. What is a Server?

A **server** is a computer or system that provides resources, data, services, or programs to other computers (called **clients**) over a network.

Servers can perform various roles, such as:

- **Web Server:** Delivers web pages (e.g., Apache, Nginx).
- **Database Server:** Stores and manages data (e.g., MySQL, MongoDB).
- **File Server:** Stores and shares files.
- **Application Server:** Runs business applications and backend logic.
- **DNS Server:** Resolves domain names to IP addresses.

Servers can be:

- **Physical (bare metal):** Dedicated hardware.
- **Virtual:** Runs on a hypervisor (e.g., VMware, VirtualBox).
- **Cloud-based:** Hosted remotely (e.g., AWS EC2, Azure VMs).
In DevOps, servers are often **automated, monitored**, and **provisioned using code** (Infrastructure as Code tools like Terraform, Ansible).

### 3. Types of Services Provided by a Cloud

Cloud computing services are divided into several models based on what is being offered:

---

#### A. Infrastructure as a Service (IaaS)

- Provides virtualized hardware resources like servers, storage, and networking.
- Users manage the operating system, middleware, and applications.
- Common Use Case: Hosting VMs, websites, custom app environments.
- Examples:
  - Amazon EC2 (AWS)
  - Google Compute Engine
  - Microsoft Azure Virtual Machines

---

#### B. Platform as a Service (PaaS)

- Offers a platform to develop, run, and manage applications without managing infrastructure.
- Providers manage the OS, runtime, and infrastructure.
- Common Use Case: Web app development, backend services.
- Examples:
  - Google App Engine
  - Heroku
  - Microsoft Azure App Services

---

#### C. Software as a Service (SaaS)

- Delivers fully developed software applications over the internet.
- Users just log in and use the application.
- Common Use Case: Email, office apps, CRM tools.
- Examples:
  - Gmail
  - Microsoft 365
  - Salesforce

---

#### Additional Models
#### Function as a Service (FaaS) / Serverless
- Run small code functions in response to events without managing servers.
- Example: AWS Lambda, Azure Functions


### 3. What is Linux?

Linux is an **open-source kernel based operating system** (OS).  It manages the computer's hardware and software and allows users to run applications and interact with the system.
- It is **free, open-source, portable and customizable**.
- Widely used in **servers, programming, DevOps, and cybersecurity**.
- It is **multi-user and multitasking**.

#### What Linux Does
- Manages **hardware resources** (CPU, memory, disk, devices).
- Provides a **command-line interface (CLI)** and optional GUI.
- Handles **user processes and permissions**.

#### Why Use Linux?
- Free and open-source.
- Secure and stable.
- Lightweight and fast.
- Preferred in **cloud, DevOps, servers, and hacking**.
- Huge community support.

#### Popular Linux Distributions (DISTROS)
- Redhat
- Ubuntu
- Detian
- Kati Linux
- CentOS 

### 4. Linux Architecture
Linux is structured into **four main layers**, each with a specific role in the system's operation.
#### 1. Hardware
- The **physical layer** of the computer.
- Includes CPU, RAM, hard disk, network cards, and other devices.
- The **kernel interacts directly** with hardware via device drivers.

#### 2. Kernel
- Kernel is a software which establish the communication between hardware and software (shell). It also converts Human language to Binary form and vice versa.
- Works directly above the hardware.
- Linux kernel is a **monolithic kernel** as well as **hybrid kernel**

#### 3. Shell
- The **interface between the user and the kernel**.
- Translates user commands into actions the kernel can execute.
- Bash( Bourne-Again Shell)
- the shell interprets and asks the kernel to execute it.

#### 4. Application Programs
- These are **software tools and user programs** used for specific tasks.
- Examples: firefox, libreoffice, vs code
- Applications interact with the **shell** or directly with system libraries.


### 5. Difference between Linux and Windows

(a) **Linux**                                 
- Open source
- Free Service
- CLI
- Customizable
- Multitasking
- Portable
- Multi-user
- Used by IT professionals
- Highest Security
- Hackable
- Virus cannot affect
- Monolithic Kernel
- Automatic updates not possible
- can schedule future jobs

(b) **Windows**
- Closed source
- Paid Service
- GUI
- Non Customizable
- Not multitasking
- Not Portable
- Single user
- IT + personal
- High Security
- Easily Hackable
- Virus can easily affect
- Hybrid Kernel
- Automatic Updates
- Cannot Schedule future jobs

### 6. Difference between Desktop OS and Server OS

(a) **Desktop OS**
- CLI/GUI
- Private
- Single user, Single Client
- High Security
- Personal use
- Customizable
- Less Updates
- Cannot scale up/scale down

(a) **Server OS**
- CLI
- Public
- Single use, Multi Client
- Highest Security
- Professional use
- Highly customizable
- more updates
- can easily scale up/scale down

### 7. Types of Kernel

(a) **MicroKernel**
- Ms-Docs, Unix, Minix
- Stable and more secure
- Easier to extend
- Stateless, without database/storage room but only had frontend and backend
- can easily debug

(b) **Monolithic**
- Linux, Windows and MacOS
- Stateful
- Harder to maintain and debug
- direct hardware access
- one bug and total destruction

 (c) **Hybrid** 
 - Linux, MacOS, windows
 - Consist of a microkernels and monolithic kernel
 - complicate to design
 - balances the performance snd the modularity

 (e) **ExoKernel**
 - MIT Exokernel (Linux, MacOS, Windows)
 - High Performance and flexible
 - Mainly used for complicated applications
 - direct access hardware

(f) **NanoKernel**
- Unix,Minix and Ms-Docs
- uses Microservices
- Embedded systems

### 8. Types of Shell in Linux
In Linux, a **shell** is a program that takes commands from the user and passes them to the **kernel** for execution. Different shells offer different features and syntaxes.

#### a. **Bourne Shell (sh)**
- The **original Unix shell**.
- Developed by **Stephen Bourne** at AT&T.
- Simple, fast, and lightweight.
- Used mainly in scripting.

#### b. **Bourne Again Shell (bash)**
- Most commonly used shell in Linux.
- Improved version of Bourne Shell.
- Developed by **GNU Project**.
- Supports command history, auto-completion, and scripting.
- Default shell in most Linux distros.

#### c. **C Shell (csh)**
- Syntax similar to the **C programming language**.
- Supports features like job control and aliases.
- Developed by **Bill Joy**.

#### d. **Korn Shell (ksh)**
- Combines features of **sh** and **csh**.
- Developed by **David Korn** at AT&T.
- Faster scripting, supports arrays and arithmetic operations.

#### e. **Z Shell (zsh)**
- Advanced shell with many user-friendly features.
- Includes features from bash, ksh, and csh.
- Popular for its customization (e.g., with **Oh My Zsh** framework).
- Used by many developers and terminal users.
