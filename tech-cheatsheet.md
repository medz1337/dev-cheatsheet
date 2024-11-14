# Complete Developer's Command Line Cheat Sheet

[TOC]

## Table of Contents
- [Linux Commands](#linux-commands)
  - [File Operations](#file-operations)
  - [System Information](#system-information)
  - [File Permissions](#file-permissions)
  - [Network](#network)
  - [Package Management](#package-management)
- [Angular CLI](#angular-cli)
  - [Project Commands](#project-commands)
  - [Generation Commands](#generation-commands)
  - [Testing Commands](#testing-commands)
- [Git & GitHub](#git--github)
  - [Basic Commands](#basic-commands)
  - [Branch Operations](#branch-operations)
  - [Advanced Operations](#advanced-operations)
- [Docker](#docker)
  - [Container Management](#container-management)
  - [Image Operations](#image-operations)
  - [Docker Compose](#docker-compose)
  - [Network Commands](#network-commands)

---

## Linux Commands

### File Operations
| Command | Description |
|---------|-------------|
| `ls` | List directory contents |
| `ls -la` | List detailed contents including hidden files |
| `pwd` | Print working directory |
| `cd [dir]` | Change directory |
| `mkdir [dir]` | Create directory |
| `rm [file]` | Remove file |
| `rm -r [dir]` | Remove directory recursively |
| `cp [src] [dest]` | Copy file or directory |
| `mv [src] [dest]` | Move or rename file |
| `touch [file]` | Create empty file |
| `cat [file]` | Display file contents |
| `less [file]` | View file with pagination |
| `head [file]` | Show first 10 lines |
| `tail [file]` | Show last 10 lines |
| `tail -f [file]` | Follow file changes |
| `nano [file]` | Edit with nano |
| `vim [file]` | Edit with vim |

### System Information
| Command | Description |
|---------|-------------|
| `top` | Show processes |
| `htop` | Interactive process viewer |
| `df -h` | Show disk usage |
| `du -sh [dir]` | Directory size |
| `free -h` | Memory usage |
| `ps aux` | List processes |
| `kill [pid]` | Kill process by ID |
| `killall [name]` | Kill process by name |

### File Permissions
| Command | Description |
|---------|-------------|
| `chmod +x [file]` | Make executable |
| `chmod 755 [file]` | Set permissions |
| `chown user [file]` | Change owner |
| `chgrp group [file]` | Change group |

### Network
| Command | Description |
|---------|-------------|
| `ping [host]` | Test connectivity |
| `wget [url]` | Download file |
| `curl [url]` | Transfer data |
| `ssh user@host` | Remote connect |
| `scp [src] [dest]` | Secure copy |
| `netstat -tulpn` | Show connections |

### Package Management
| Command | Description |
|---------|-------------|
| `apt update` | Update package list |
| `apt upgrade` | Upgrade packages |
| `apt install [pkg]` | Install package |
| `apt remove [pkg]` | Remove package |
| `apt search [pkg]` | Search packages |

---

## Angular CLI

### Project Commands
| Command | Description |
|---------|-------------|
| `ng new [name]` | New project |
| `ng serve` | Start dev server |
| `ng build` | Build app |
| `ng build --prod` | Production build |

### Generation Commands
| Command | Description |
|---------|-------------|
| `ng g c [name]` | Generate component |
| `ng g s [name]` | Generate service |
| `ng g p [name]` | Generate pipe |
| `ng g d [name]` | Generate directive |
| `ng g g [name]` | Generate guard |

### Testing Commands
| Command | Description |
|---------|-------------|
| `ng test` | Run unit tests |
| `ng e2e` | Run e2e tests |
| `ng lint` | Run linter |

---

## Git & GitHub

### Basic Commands
| Command | Description |
|---------|-------------|
| `git init` | Initialize repo |
| `git clone [url]` | Clone repo |
| `git status` | Check status |
| `git add [file]` | Stage file |
| `git add .` | Stage all |
| `git commit -m "[msg]"` | Commit changes |
| `git push origin [branch]` | Push to remote |
| `git pull origin [branch]` | Pull from remote |

### Branch Operations
| Command | Description |
|---------|-------------|
| `git branch` | List branches |
| `git branch [name]` | Create branch |
| `git checkout [branch]` | Switch branch |
| `git checkout -b [name]` | Create & switch |
| `git merge [branch]` | Merge branch |
| `git branch -d [name]` | Delete branch |

### Advanced Operations
| Command | Description |
|---------|-------------|
| `git log` | View history |
| `git diff` | View changes |
| `git stash` | Stash changes |
| `git stash pop` | Apply stash |
| `git reset --hard HEAD` | Reset to last commit |
| `git rebase [branch]` | Rebase branch |

---

## Docker

### Container Management
| Command | Description |
|---------|-------------|
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker start [container]` | Start container |
| `docker stop [container]` | Stop container |
| `docker rm [container]` | Remove container |
| `docker logs [container]` | View logs |
| `docker exec -it [container] bash` | Container shell |

### Image Operations
| Command | Description |
|---------|-------------|
| `docker images` | List images |
| `docker pull [image]` | Pull image |
| `docker build -t [name] .` | Build image |
| `docker rmi [image]` | Remove image |
| `docker push [image]` | Push image |

### Docker Compose
| Command | Description |
|---------|-------------|
| `docker-compose up` | Start services |
| `docker-compose down` | Stop services |
| `docker-compose build` | Build services |
| `docker-compose logs` | View logs |

### Network Commands
| Command | Description |
|---------|-------------|
| `docker network ls` | List networks |
| `docker network create` | Create network |
| `docker network connect` | Connect container |
| `docker network rm` | Remove network |

---

## Useful Tips & Tricks

### Command Line Shortcuts
- `Ctrl + C` - Interrupt command
- `Ctrl + Z` - Suspend command
- `Ctrl + D` - Exit shell
- `Ctrl + L` - Clear screen
- `Ctrl + R` - Search history
- `Ctrl + A` - Start of line
- `Ctrl + E` - End of line
- `Tab` - Auto-complete
- `!!` - Repeat last command

### Common Command Combinations
```bash
# Search files
find . -name "*.txt" | xargs grep "search-term"

# Monitor logs
tail -f log.txt | grep "error"

# Disk usage by directory
du -sh * | sort -hr

# Find largest files
find . -type f -exec du -h {} + | sort -hr | head -n 10

# Kill process using port
lsof -i :3000 | awk '{print $2}' | tail -n1 | xargs kill

# Git: Undo last commit
git reset --soft HEAD~1

# Docker: Clean unused resources
docker system prune -a

# Angular: Generate module with routing
ng g m features/user --routing
```

### Environment Variables
```bash
# Set variable
export VAR_NAME=value

# Read variable
echo $VAR_NAME

# List all variables
printenv

# Add to PATH
export PATH=$PATH:/new/path
```

### File Permissions Quick Reference
```bash
chmod commands:
4 = read (r)
2 = write (w)
1 = execute (x)

Example:
chmod 755 file
# Owner: rwx = 7
# Group: r-x = 5
# Others: r-x = 5
```

---

## Notes
- This cheat sheet is designed for quick reference
- Commands may vary slightly between different OS versions
- Always check documentation for specific versions
- Back up data before running destructive commands
- Use `--help` or `man` for detailed command information

