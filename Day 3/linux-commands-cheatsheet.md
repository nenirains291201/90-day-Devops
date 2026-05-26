# LINUX COMMANDS CHEATSHEET

# PROCESS MANAGEMENT


# Show running processes
ps
ps aux

# Live process monitoring
top
htop

# Find a process
ps aux | grep process_name

# Kill processes
kill PID
kill -9 PID
killall process_name

# Change process priority
nice -n 10 command
renice 10 -p PID

------------------------------------------
# FILE SYSTEM COMMANDS

# List files and directories
ls
ls -l
ls -a

# Change directory
cd folder_name
cd ..
cd ~

# Show current directory
pwd

# Create files and folders
touch file.txt
mkdir folder_name
mkdir folder1 folder2
mkdir -p parent/child

# Copy, move, delete
cp file1 file2
mv file1 folder/
rm file.txt
rm -r folder_name

# Search files
find /path -name file.txt
locate file.txt

# Permissions
chmod 755 file.sh
chown user:group file.txt

-----------------------------------------------
# NETWORKING COMMANDS

# Check internet connection
ping google.com

# Show IP address
ip a

# Download or fetch data
curl https://example.com
wget https://example.com/file

# Check network connections / ports
ss -tulnp
netstat -tulnp

# Trace network route
traceroute google.com

# DNS lookup
nslookup google.com
dig google.com


-------------------------
# SYSTEM INFO

# Disk usage
df -h
du -sh folder_name

# Memory usage
free -h

# System information
uname -a

-------------------------
# HELP COMMAND

# Manual for any command
man command_name