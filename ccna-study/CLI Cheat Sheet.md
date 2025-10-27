# Cisco IOS Command Cheat Sheet

## Mode Navigation & Access

| Command                         | Purpose                                      |
|----------------------------------|----------------------------------------------|
| logout / exit / quit            | Exit User EXEC mode                          |
| enable                          | Enter Privileged EXEC mode                   |
| disable                         | Return to User EXEC mode                     |
| configure terminal              | Enter Global Configuration mode              |
| exit / end / Ctrl-Z             | Exit configuration modes                     |
| interface [type/number]         | Enter Interface Configuration mode           |

## Interface & Device Configuration

| Command                         | Purpose                                      |
|----------------------------------|----------------------------------------------|
| description [text]              | Add description to interface                 |
| no shutdown                     | Enable an interface                          |
| hostname [name]                 | Change device hostname                       |
| clock timezone [zone] [offset] | Set timezone                                 |
| no ip domain-lookup             | Disable DNS lookup on mistyped commands      |
| duplex full                     | Set full-duplex mode                         |
| duplex half                     | Set half-duplex mode                         |
| duplex auto                     | Enable autonegotiation for duplex mode       |
| speed 10                        | Set interface speed to 10 Mbps               |
| speed 100                       | Set interface speed to 100 Mbps              |
| speed 1000                      | Set interface speed to 1000 Mbps             |

## Show Commands & Filtering

| Command                                         | Purpose                                      |
|--------------------------------------------------|----------------------------------------------|
| show running-config                              | Display current running configuration        |
| show startup-config                              | Display startup configuration in NVRAM       |
| show ip route                                    | Display routing table                        |
| show clock                                       | Display system clock                         |
| show ip interface brief                          | Display summary of interface status          |
| show running-config | include [string]           | Show lines that include a specific string    |
| show running-config | begin [string]             | Start output from matching line              |
| show running-config | section [string]           | Show full section starting with match        |
| show running-config | exclude [string]           | Exclude lines matching expression            |
| show interface [int] | include address           | Show MAC address of specific interface       |
| show mac address-table                           | Display MAC address table on switch          |
| show interfaces [type slot/port]                 | Display detailed interface statistics        |
| show version                                     | Display IOS version, uptime, platform info   |
| show running-config                              | Display active configuration including IP    |

## Configuration Management

| Command                                 | Purpose                                      |
|------------------------------------------|----------------------------------------------|
| copy running-config startup-config       | Save running config to startup config        |
| copy startup-config running-config       | Merge startup config into running config     |
| copy running-config tftp:                | Backup running config to TFTP server         |
| erase startup-config                     | Delete startup config from NVRAM             |
| reload                                   | Reboot the device                            |

## CLI Help & Syntax Assistance

| Command / Key Combo                     | Purpose                                      |
|------------------------------------------|----------------------------------------------|
| ?                                        | Show available commands (context-sensitive)  |
| show ?                                   | Show syntax options for show command         |
| s? , sh? , show r?                       | List commands starting with specific letters |
| Tab                                      | Auto-complete command words                  |
| con + Tab                                | Attempt to auto-complete configure           |
| ^ (caret symbol)                         | Indicates location of syntax error           |

## Command-Line Editing Keys

| Key Combo         | Function                                      |
|-------------------|-----------------------------------------------|
| Ctrl-A            | Move cursor to beginning of line              |
| Ctrl-E            | Move cursor to end of line                    |
| Ctrl-B / Ctrl-F   | Move cursor backward/forward one character    |
| Esc-B / Esc-F     | Move cursor backward/forward one word         |
| Backspace         | Delete character to the left                  |
| Ctrl-D            | Delete character at cursor                    |
| Ctrl-R            | Redisplay current command line                |
| Ctrl-U            | Erase entire line                             |
| Ctrl-W            | Erase word to the left                        |
| Ctrl-C            | Abort current command and exit config mode    |
| Ctrl-Shift-6      | Interrupt IOS process (e.g. ping)             |
| Ctrl-P / Up Arrow | Recall previous commands                      |
| Ctrl-N / Down Arrow | Recall more recent commands                 |

## Terminal Settings

| Command                         | Purpose                                      |
|----------------------------------|----------------------------------------------|
| terminal history [size]         | Set command history buffer size              |
| terminal length [number]        | Set number of lines before CLI pauses output |

## MAC Table & Traffic Commands

| Command                                 | Purpose                                      |
|----------------------------------------|----------------------------------------------|
| clear mac address-table dynamic        | Clear dynamic MAC entries                    |
| ping [IP address]                      | Send ICMP Echo to generate traffic           |