# Nmap -- Network Discovery and Security Auditing

**Author:** Jeremiah Alexander\
**Course:** CYB 301 -- Hacker's Toolbox Project\
**Tool:** Nmap (Network Mapper)\
**Operating System:** Windows 10/11\
**Project:** Part II -- Tutorial and Lab Demonstration

------------------------------------------------------------------------

## 1. Overview

Nmap (Network Mapper) is an open-source network discovery and security
auditing tool used to examine networks and identify information about
connected systems.

It allows cybersecurity professionals to discover hosts, identify open
ports, detect running services, and gather information about network
configurations.

This project demonstrates the installation and practical use of Nmap on
a Windows computer. The lab focuses on scanning the local machine using
the loopback address `127.0.0.1`.

## 2. Purpose of Nmap

Nmap is commonly used for:

-   Network discovery and host identification.
-   TCP and UDP port scanning.
-   Service and version detection.
-   Operating system detection.
-   Network inventory management.
-   Authorized security assessments and reconnaissance.

## 3. Installation Requirements

**Requirements:**

-   Windows 10 or Windows 11.
-   Internet connection for downloading Nmap.
-   Administrator permissions may be required for installation and
    certain scanning features.
-   Npcap for packet-capture functionality used by applicable Nmap
    features.

**Download:** [Nmap for Windows](https://nmap.org/download.html)

### Installation Instructions

1.  Visit the official Nmap download page.
2.  Select the Windows installer.
3.  Download the latest stable release.
4.  Open the downloaded installer.
5.  Follow the installation wizard.
6.  Install Npcap if prompted.
7.  Open Command Prompt or PowerShell.
8.  Verify the installation using:

``` powershell
nmap --version
```

## 4. Basic Usage

The following commands demonstrate some of Nmap's most useful features
on Windows.

### Verify Installation

``` powershell
nmap --version
```

Displays the installed Nmap version.

### Display Network Configuration

``` cmd
ipconfig
```

Displays local network configuration, including IP addresses and subnet
information.

### Host Discovery

``` powershell
nmap -sn 127.0.0.1
```

Checks whether the local machine is available without performing a port
scan.

### Basic TCP Port Scan

``` powershell
nmap 127.0.0.1
```

Scans the most common 1,000 TCP ports on the local machine by default.

### Service and Version Detection

``` powershell
nmap -sV 127.0.0.1
```

Attempts to identify the services and software versions associated with
discovered open ports.

### Save Scan Results

``` powershell
nmap -sV -oN nmap-localhost-results.txt 127.0.0.1
```

Saves the scan output in a readable text file.

### Open Saved Results in Notepad

``` powershell
notepad nmap-localhost-results.txt
```

Opens the saved scan output in Windows Notepad for review.

## 5. Lab Demonstration

**Lab Objective:** Demonstrate how Nmap can be used to examine a
computer's network services and identify TCP port states.

**Environment:**

-   Operating System: Windows 10/11.
-   Tool: Nmap.
-   Target: `127.0.0.1` (localhost).
-   Scan Type: Host discovery, TCP port scanning, and service detection.

### Demonstration Workflow

1.  Verify that Nmap is installed.
2.  Examine the computer's network configuration.
3.  Perform host discovery against localhost.
4.  Perform a default TCP port scan.
5.  Use service detection to examine open ports.
6.  Save the scan results for documentation and analysis.
7.  Open the saved results in Notepad.

### Understanding the Results

Nmap identifies different port states:

  -----------------------------------------------------------------------
  State                               Meaning
  ----------------------------------- -----------------------------------
  Open                                An application is accepting
                                      connections on the port.

  Closed                              The port is reachable, but no
                                      application is listening.

  Filtered                            Nmap cannot determine whether the
                                      port is open because filtering or
                                      another obstacle prevents a
                                      definitive result.
  -----------------------------------------------------------------------

The scan results depend on the services running on the computer and on
local firewall or network settings. A scan may show no open ports, and
that is a valid result. The findings can help administrators identify
exposed services and review their security configurations.

## 6. Strengths and Limitations

### Strengths

-   Free and open source.
-   Widely used in the cybersecurity industry.
-   Supports multiple scanning techniques.
-   Provides service and version detection.
-   Offers flexible command-line options.
-   Supports multiple operating systems.

### Limitations

-   Does not automatically identify every vulnerability.
-   Scan results can be affected by firewalls and network filtering.
-   Some scanning features require administrator privileges.
-   Service and version detection are not always completely accurate.
-   Requires authorization and responsible use.

## 7. Professional Applications

Nmap can be used by:

-   Network administrators conducting network inventories.
-   Security analysts investigating exposed network services.
-   Penetration testers performing authorized reconnaissance.
-   Cybersecurity teams reviewing network configurations.
-   IT professionals troubleshooting network connectivity.

## 8. Video Demonstration
 Nmap Network Discovery and Security Auditing -- CYB 301

[https://youtu.be/MIYuBSvr1OM](https://youtu.be/MIYuBSvr1OM)

The video demonstrates Nmap installation, verification, local host
discovery, TCP port scanning, service detection, and scan-result
analysis.

.

## 10. References and Resources

1.  [Nmap Official Website](https://nmap.org/)
2.  [Nmap Reference Guide](https://nmap.org/book/man.html)
3.  [Nmap Download Page](https://nmap.org/download.html)
4.  [Nmap Network Scanning Documentation](https://nmap.org/book/)
5.  [Npcap Official Website](https://npcap.com/)

