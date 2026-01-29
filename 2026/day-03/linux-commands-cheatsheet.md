Process Management

ps aux – Shows all running processes with details

top – Displays live CPU and memory usage

htop – Interactive process viewer (better than top)

uptime – Shows system running time and load

kill PID – Gracefully stops a process

kill -9 PID – Forcefully kills a process
-------------------------------------
 File & Directory

pwd – Shows current directory path

ls -l – Lists files with permissions and details

mkdir dir – Creates a new directory

mkdir -p a/b/c – Creates nested directories

touch file – Creates an empty file

cp file1 file2 – Copies a file

mv old new – Moves or renames a file

rm file – Deletes a file

rm -rf dir – Force deletes a directory
------------------------------------------
 Disk & Memory

df -h – Shows disk space usage

du -sh * – Shows size of files/folders

free -m – Shows RAM usage
----------------------------------------------
 Logs & Viewing

cat file – Displays file content

less file – Views large files page by page

head file – Shows first 10 lines

tail file – Shows last 10 lines

tail -f log – Monitors log file live

-------------------------------------------------

 Search & Filter

grep word file – Searches word in file

grep -i word file – Case-insensitive search

grep -r word /path – Searches recursively

wc -l file – Counts lines

wc -w file – Counts words
-------------------------------------------------
 Networking

ping host – Checks network connectivity

ip addr – Shows system IP address

curl url – Tests website or API response
---------------------------------------------------
 Permissions

ls -l – Checks file permissions

chmod 755 file – Changes file permissions

chown user:group file – Changes file owner
