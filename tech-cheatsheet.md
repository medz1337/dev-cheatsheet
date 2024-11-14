# Developer's Command Line Cheat Sheet

## Table of Contents
- [File Operations](#file-operations)
  - [File Content](#file-content)
  - [File Permissions](#file-permissions)
- [System Management](#system-management)
  - [Process Management](#process-management)
  - [System Information](#system-information)
  - [Disk Management](#disk-management)
  - [User Management](#user-management)
- [Network Commands](#network-commands)
- [Package Management](#package-management)
  - [APT (Ubuntu/Debian)](#apt-ubuntudebian)
  - [DNF (Fedora)](#dnf-fedora)
  - [Archive Commands](#archive-commands)
- [Git & GitHub](#git--github)
- [Docker](#docker)
- [Angular CLI](#angular-cli)
- [Node.js & Express](#nodejs--express)
  - [Node.js Commands](#nodejs-commands)
  - [Express Generator](#express-generator)
  - [Express Application Structure](#express-application-structure)
  - [Common Express Code Snippets](#common-express-code-snippets)
- [PostgreSQL](#postgresql)
  - [Server Management](#server-management)
  - [Database Operations](#database-operations)
  - [Table Operations](#table-operations)
  - [Query Commands](#query-commands)
- [Keyboard Shortcuts](#keyboard-shortcuts)


- [File Operations](#file-operations)
- [System Management](#system-management)
- [Network Commands](#network-commands)
- [Package Management](#package-management)
- [Git & GitHub](#git--github)
- [Docker](#docker)
- [Angular CLI](#angular-cli)

## File Operations
| Command | Description |
|---------|-------------|
| `ls` | List directory contents |
| `ls -l` | Long format listing with details |
| `ls -a` | Show hidden files |
| `ls -la` | List detailed contents including hidden files |
| `pwd` | Print working directory |
| `cd [dir]` | Change directory |
| `mkdir [dir]` | Create directory |
| `rmdir [dir]` | Remove empty directory |
| `rm [file]` | Remove file |
| `rm -r [dir]` | Remove directory and contents |
| `cp [src] [dest]` | Copy file or directory |
| `mv [src] [dest]` | Move or rename file |
| `touch [file]` | Create empty file |
| `find [dir] -name "[pattern]"` | Search for files |

### File Content
| Command | Description |
|---------|-------------|
| `cat [file]` | Display file contents |
| `tac [file]` | Display file contents in reverse |
| `less [file]` | View file with pagination |
| `head -n [num] [file]` | View first n lines |
| `tail -n [num] [file]` | View last n lines |
| `tail -f [file]` | Follow file changes |
| `nano [file]` | Edit with nano |
| `vim [file]` | Edit with vim |
| `grep "[pattern]" [file]` | Search in file |
| `grep -r "[pattern]" [dir]` | Search in directory |

### File Permissions
| Command | Description |
|---------|-------------|
| `chmod +x [file]` | Make executable |
| `chmod 755 [file]` | Set rwxr-xr-x permissions |
| `chown [user]:[group] [file]` | Change owner and group |
| `chgrp [group] [file]` | Change group ownership |

## System Management

### Process Management
| Command | Description |
|---------|-------------|
| `ps aux` | List all processes |
| `top` | Show processes |
| `htop` | Interactive process viewer |
| `kill [pid]` | Kill process by ID |
| `killall [name]` | Kill process by name |
| `systemctl start [service]` | Start service |
| `systemctl stop [service]` | Stop service |

### System Information
| Command | Description |
|---------|-------------|
| `uname -a` | System information |
| `hostname` | Show/set hostname |
| `uptime` | System uptime |
| `free -h` | Memory usage |
| `df -h` | Show disk usage |
| `du -sh [dir]` | Directory size |
| `lscpu` | CPU details |

### Disk Management
| Command | Description |
|---------|-------------|
| `mount [device] [mountpoint]` | Mount device |
| `umount [mountpoint]` | Unmount device |
| `fdisk -l` | List partitions |
| `mkfs.ext4 [device]` | Format as EXT4 |

### User Management
| Command | Description |
|---------|-------------|
| `whoami` | Show current user |
| `who` | Show logged-in users |
| `adduser [user]` | Add new user |
| `passwd [user]` | Change password |
| `sudo [command]` | Run as superuser |

## Network Commands
| Command | Description |
|---------|-------------|
| `ping [host]` | Test connectivity |
| `curl [url]` | Transfer data |
| `wget [url]` | Download file |
| `ssh user@host` | Remote connect |
| `scp [src] [dest]` | Secure copy |
| `netstat -tulpn` | Show connections |
| `ifconfig` | Network interface details |
| `ip a` | Show IP address details |

## Package Management

### APT (Ubuntu/Debian)
| Command | Description |
|---------|-------------|
| `apt update` | Update package list |
| `apt upgrade` | Upgrade packages |
| `apt install [pkg]` | Install package |
| `apt remove [pkg]` | Remove package |
| `apt search [pkg]` | Search packages |

### DNF (Fedora)
| Command | Description |
|---------|-------------|
| `dnf install [pkg]` | Install package |
| `dnf update` | Update packages |
| `dnf remove [pkg]` | Remove package |
| `dnf search [keyword]` | Search packages |

### Archive Commands
| Command | Description |
|---------|-------------|
| `tar -cvf [file.tar] [dir]` | Create tar |
| `tar -xvf [file.tar]` | Extract tar |
| `tar -zcvf [file.tar.gz] [dir]` | Create compressed tar |
| `tar -zxvf [file.tar.gz]` | Extract compressed tar |
| `gzip [file]` | Compress file |
| `gunzip [file.gz]` | Decompress file |

## Git & GitHub
| Command | Description |
|---------|-------------|
| `git init` | Initialize repo |
| `git clone [url]` | Clone repo |
| `git add [file]` | Stage file |
| `git add .` | Stage all changes |
| `git commit -m "[msg]"` | Commit changes |
| `git status` | Check status |
| `git pull` | Pull changes |
| `git push` | Push changes |
| `git branch` | List branches |
| `git checkout [branch]` | Switch branch |
| `git merge [branch]` | Merge branch |
| `git log` | View history |
| `git diff` | View changes |
| `git stash` | Stash changes |
| `git reset --hard HEAD` | Reset to last commit |

## Docker
| Command | Description |
|---------|-------------|
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker images` | List images |
| `docker pull [image]` | Pull image |
| `docker build -t [name] .` | Build image |
| `docker run [image]` | Run container |
| `docker stop [container]` | Stop container |
| `docker rm [container]` | Remove container |
| `docker rmi [image]` | Remove image |
| `docker exec -it [container] bash` | Container shell |
| `docker-compose up` | Start services |
| `docker-compose down` | Stop services |

## Angular CLI
| Command | Description |
|---------|-------------|
| `ng new [name]` | Create project |
| `ng serve` | Start dev server |
| `ng build` | Build app |
| `ng test` | Run tests |
| `ng g c [name]` | Generate component |
| `ng g s [name]` | Generate service |
| `ng g p [name]` | Generate pipe |
| `ng g d [name]` | Generate directive |

## Node.js & Express

### Node.js Commands
| Command | Description |
|---------|-------------|
| `node [file]` | Run a JavaScript file |
| `node --version` | Check Node.js version |
| `nvm ls` | List installed Node versions |
| `nvm use [version]` | Switch Node version |
| `nvm install [version]` | Install Node version |
| `npm init` | Initialize new project |
| `npm init -y` | Initialize with defaults |
| `npm install` | Install dependencies |
| `npm i [package]` | Install package |
| `npm i -g [package]` | Install package globally |
| `npm i --save-dev [package]` | Install dev dependency |
| `npm uninstall [package]` | Remove package |
| `npm update` | Update packages |
| `npm run [script]` | Run script from package.json |
| `npm start` | Run start script |
| `npm test` | Run test script |
| `npm list` | List installed packages |
| `npm outdated` | Check outdated packages |
| `npm audit` | Check security vulnerabilities |
| `npm audit fix` | Fix security issues |

### Express Generator
| Command | Description |
|---------|-------------|
| `npx express-generator [app]` | Create new Express app |
| `npx express-generator --view=ejs` | Create with EJS template |
| `npx express-generator --git` | Create with .gitignore |

### Express Application Structure
```bash
myapp/
  ├── app.js          # Application entry point
  ├── bin/            # Startup scripts
  │   └── www         # Server configuration
  ├── public/         # Static files
  │   ├── images/     # Image files
  │   ├── javascripts/# Client-side JavaScript
  │   └── stylesheets/# CSS files
  ├── routes/         # Route handlers
  │   ├── index.js    # Main routes
  │   └── users.js    # User routes
  ├── views/          # Template files
  ├── package.json    # Project metadata
  └── node_modules/   # Dependencies
```

### Common Express Code Snippets

#### Basic Express Server
```javascript
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});
```

#### Middleware Setup
```javascript
// Body parser middleware
app.use(express.json());
app.use(express.urlencoded({ extended: true }));

// Static files middleware
app.use(express.static('public'));

// Custom middleware
app.use((req, res, next) => {
  console.log(`${req.method} ${req.path}`);
  next();
});
```

#### Route Handlers
```javascript
// Basic route
app.get('/api/items', (req, res) => {
  res.json(items);
});

// Route with parameters
app.get('/api/items/:id', (req, res) => {
  const id = req.params.id;
  res.json(items[id]);
});

// POST request handler
app.post('/api/items', (req, res) => {
  const newItem = req.body;
  items.push(newItem);
  res.status(201).json(newItem);
});

// Router module
const router = express.Router();
router.get('/', (req, res) => {
  res.send('Router working');
});
app.use('/api', router);
```

#### Error Handling
```javascript
// Error handling middleware
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something broke!');
});

// 404 handler
app.use((req, res, next) => {
  res.status(404).send('Not found');
});
```

#### Database Connection (MongoDB example)
```javascript
const mongoose = require('mongoose');
mongoose.connect('mongodb://localhost/myapp', {
  useNewUrlParser: true,
  useUnifiedTopology: true
});

// Check connection
const db = mongoose.connection;
db.on('error', console.error.bind(console, 'connection error:'));
db.once('open', () => {
  console.log('Database connected');
});
```

### Express Environment Setup
```bash
# Development
npm install nodemon --save-dev
npm install dotenv --save

# Add to package.json
{
  "scripts": {
    "start": "node app.js",
    "dev": "nodemon app.js"
  }
}

# Create .env file
PORT=3000
MONGODB_URI=mongodb://localhost/myapp
NODE_ENV=development
```

## PostgreSQL

### Server Management
| Command | Description |
|---------|-------------|
| `sudo service postgresql start` | Start PostgreSQL server |
| `sudo service postgresql stop` | Stop PostgreSQL server |
| `sudo service postgresql restart` | Restart PostgreSQL server |
| `pg_ctl status` | Check server status |
| `psql --version` | Check PostgreSQL version |

### Database Operations
| Command | Description |
|---------|-------------|
| `psql -U [username]` | Connect as user |
| `psql -d [database]` | Connect to specific database |
| `createdb [dbname]` | Create new database |
| `dropdb [dbname]` | Delete database |
| `pg_dump [dbname] > [file]` | Backup database |
| `psql [dbname] < [file]` | Restore database |

### PSQL Shell Commands
| Command | Description |
|---------|-------------|
| `\l` | List all databases |
| `\c [dbname]` | Connect to database |
| `\dt` | List all tables |
| `\d [table]` | Describe table |
| `\du` | List all users |
| `\dn` | List all schemas |
| `\df` | List all functions |
| `\dv` | List all views |
| `\x` | Toggle expanded display |
| `\timing` | Toggle timing |
| `\q` | Quit psql |
| `\?` | Show psql commands |
| `\h` | SQL command help |

### Table Operations
```sql
-- Create table
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Modify table
ALTER TABLE users ADD COLUMN age INTEGER;
ALTER TABLE users DROP COLUMN age;
ALTER TABLE users ALTER COLUMN name TYPE VARCHAR(200);

-- Delete table
DROP TABLE users;

-- Indexes
CREATE INDEX idx_user_email ON users(email);
DROP INDEX idx_user_email;
```

### Query Commands
```sql
-- Basic queries
SELECT * FROM users;
SELECT name, email FROM users WHERE age > 18;
SELECT * FROM users ORDER BY created_at DESC LIMIT 10;

-- Insert data
INSERT INTO users (name, email) VALUES ('John', 'john@example.com');

-- Update data
UPDATE users SET name = 'Johnny' WHERE id = 1;

-- Delete data
DELETE FROM users WHERE id = 1;

-- Joins
SELECT 
    users.name, 
    orders.order_date
FROM users
JOIN orders ON users.id = orders.user_id;

-- Group by
SELECT 
    country,
    COUNT(*) as user_count
FROM users
GROUP BY country
HAVING COUNT(*) > 10;

-- Transactions
BEGIN;
UPDATE accounts SET balance = balance - 100 WHERE id = 1;
UPDATE accounts SET balance = balance + 100 WHERE id = 2;
COMMIT;

-- Views
CREATE VIEW active_users AS
SELECT * FROM users WHERE last_login > NOW() - INTERVAL '30 days';
```

### User Management
```sql
-- Create user
CREATE USER username WITH PASSWORD 'password';

-- Grant privileges
GRANT ALL PRIVILEGES ON DATABASE dbname TO username;
GRANT SELECT, INSERT ON tablename TO username;

-- Revoke privileges
REVOKE ALL PRIVILEGES ON DATABASE dbname FROM username;

-- Alter user
ALTER USER username WITH PASSWORD 'newpassword';

-- Delete user
DROP USER username;
```

### Backup and Restore
```bash
# Backup database
pg_dump dbname > backup.sql
pg_dump -Fc dbname > backup.dump  # Compressed format

# Backup specific tables
pg_dump -t tablename dbname > table_backup.sql

# Restore database
psql dbname < backup.sql
pg_restore -d dbname backup.dump  # For compressed format

# Backup with options
pg_dump -h localhost -U username -W -F t dbname > backup.tar
```

### Common Patterns

#### Connection String
```
postgresql://username:password@localhost:5432/dbname
```

#### Node.js Connection (using node-postgres)
```javascript
const { Pool } = require('pg');
const pool = new Pool({
  user: 'username',
  host: 'localhost',
  database: 'dbname',
  password: 'password',
  port: 5432,
});

// Query example
const query = 'SELECT * FROM users WHERE id = $1';
const values = [userId];
const result = await pool.query(query, values);
```

#### Environment Variables
```bash
export PGHOST=localhost
export PGPORT=5432
export PGUSER=username
export PGPASSWORD=password
export PGDATABASE=dbname
```

## Keyboard Shortcuts
| Shortcut | Description |
|----------|-------------|
| `Ctrl + C` | Cancel command |
| `Ctrl + Z` | Suspend process |
| `Ctrl + D` | Exit shell |
| `Ctrl + L` | Clear screen |
| `Ctrl + R` | Search history |
| `Ctrl + A` | Start of line |
| `Ctrl + E` | End of line |
| `Tab` | Auto-complete |
| `!!` | Repeat last command |

