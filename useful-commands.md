### show active TCP/UDP network connections, listening ports, and associated processes with their PID and program names ###
sudo netstat -tulpn

### displays disk space usage, including hidden, in human-readable format ###
df -ah /path/to/directory

### detailed information about the system, including the kernel name, version, release, machine hardware, processor type, and operating system ###
uname -a

### info on network interfaces on system - IP's, network masks, status ###
ip addr show

###  ###

### Check last modification time ###
ls -laht path/

### Show Large Dirs ###
du ./* -hac | sort -rh | head -15

### Install Homebrew ###
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

### migrate folder (manual migration) ###
rsync -zvhr -t /path/to/source-folder/wp-content/ /path/to/dest-folder/wp-content/

### move folder contents up a level ###
mv myfolder/* .

### say yes/no to all ###
echo "no" | COMMAND

### Disk usage by a specific file type ###
find . -type f -iname "*.FILETYPE" -exec du -ch {} + | grep -E "total$"

### manually search mysql slow queries ###
grep "Schema: [wp_|snapshot_]" /var/log/mysql/mysql-slow.log | awk '{print $3}' | sort | uniq -c | sort -rn

### Nano with line numbers shown ###
nano --linenumbers file.txt

### parse log files for top user agents ###
zcat LOGZIPFILE 2>/dev/null | cut -d'"' -f6 | sort | uniq -c | sort -rn | head -20
OR for non-zip
cat /var/log/path/LOGFILE | cut -d'"' -f6 | sort | uniq -c | sort -rn | head -20

