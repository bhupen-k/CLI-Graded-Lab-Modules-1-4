1. User Identity Verification:
   
Commands:   

whoami

groups

Outputs:

bhupen

staff everyone localaccounts _appserverusr admin _appserveradm _lpadmin com.apple.sharepoint.group.1 _appstore _lpoperator _developer _analyticsusers com.apple.access_ftp com.apple.access_screensharing com.apple.access_ssh com.apple.access_remote_ae

Explanation: 
The whoami command displays the currently logged-in user. The groups command shows all the groups my user account belongs to, confirming my identity and permissions.
Screenshot:
<img width="1137" height="287" alt="Screenshot 2026-01-05 at 10 39 03 PM" src="https://github.com/user-attachments/assets/0b78c0cc-71b1-472b-8d26-679da3322abd" />

2. Workspace Validation:

Commands:

pwd

ls -l

Outputs:

/Users/bhupen/Documents
total 60808
-rw-r--r--@   1 bhupen  staff   3782496 Nov 21  2022 AUDIO-2022-10-18-19-46-40.mp3
drwxr-xr-x    8 bhupen  staff       256 Oct 23 23:00 Adobe
drwxr-xr-x   18 bhupen  staff       576 Jan 29  2025 Adobe Fonts
drwxr-xr-x   25 bhupen  staff       800 May  3  2025 Assets
-rw-r--r--@   1 bhupen  staff    173167 Aug 21  2024 Damage and Defective 17 July to 19 Aug.pdf
-rw-r--r--@   1 bhupen  staff    211683 Aug 21  2024 Damage and Defective 2 Jun to 15 July.pdf
drwxr-xr-x    4 bhupen  staff       128 Dec 30 13:00 Finance YT
drwxr-xr-x   12 bhupen  staff       384 Sep  9 15:43 Framer Template Photos
-rw-r--r--@   1 bhupen  staff     17186 Jul 15 12:56 How to Plan a Website Like a Pro — Without Touching a Design Tool .docx
drwxr-xr-x@   4 bhupen  staff       128 Jan  5 22:26 JavaDirectory
drwxr-xr-x    4 bhupen  staff       128 Oct 12 11:19 Magazines
-rw-r--r--    1 bhupen  staff       194 Feb 12  2025 Media Browser Provider Exception
drwxr-xr-x    6 bhupen  staff       192 Feb  6  2025 Motion Graphics and Animations
-rw-r--r--@   1 bhupen  staff   2924092 Mar 26  2025 Part 2.m4a
-rw-r--r--@   1 bhupen  staff    308283 Oct  8  2024 RAJASTHAN_10_5 2.numbers
-rw-r--r--@   1 bhupen  staff     23894 Oct  8  2024 Rate Chart (Jodhpur).pdf
-rw-r--r--    1 bhupen  staff       172 Feb 12  2025 Recent Directories
drwxr-xr-x   12 bhupen  staff       384 Jan 26  2025 SAMPLE
-rw-r--r--    1 bhupen  staff       156 Feb 12  2025 SharedView Column Settings
-rw-r--r--@   1 bhupen  staff   1069017 Aug 31  2024 Stock Record updated till 31 Aug.pdf
-rw-r--r--@   1 bhupen  staff    196161 Oct 13  2024 Untitled 3.numbers
drwxr-xr-x@ 156 bhupen  staff      4992 Apr 10  2025 Whatsapp Chats
drwxr-xr-x@   5 bhupen  staff       160 Apr 23  2025 Wondershare
-rw-r--r--@   1 bhupen  staff     79236 Dec 25  2023 confidence interval question.pdf
-rw-r--r--@   1 bhupen  staff  22316829 Feb 13  2025 webflow b roll wo audio.mov

Explanation:

The pwd command displays the current working directory. The ls -l command lists all files and directories in long format, showing permissions, ownership, and sizes.

Screenshot:<img width="1136" height="465" alt="Screenshot 2026-01-05 at 10 53 06 PM" src="https://github.com/user-attachments/assets/3849ecca-a3a6-4bad-ab4c-9687d19cd9e3" />

3. Environment Confirmation File

Command:

echo "Linux user environment verified" > user_info.txt

cat user_info.txt

Outputs:

Linux user environment verified

Explanation:

This command creates a file named user_info.txt and writes a confirmation message into it. The file content is verified using the cat command

Screenshot: <img width="706" height="87" alt="Screenshot 2026-01-05 at 10 56 49 PM" src="https://github.com/user-attachments/assets/5b3bbe1c-a04c-4a6d-ab4c-e36f02952d09" />

4. File Integrity Check

Commands:

wc -c user_info.txt

Outputs:

32 user_info.txt

Explanation:

The wc -c command counts the number of characters present in the file, verifying the file’s content length.

Screenshot:
<img width="562" height="52" alt="Screenshot 2026-01-05 at 10 58 50 PM" src="https://github.com/user-attachments/assets/a43af20b-9571-4f81-933c-57744e6f4157" />

5. Learning the tools:

Commands:

man mkdir

Output:

MKDIR(1)                                                          General Commands Manual                                                          MKDIR(1)

NAME
     mkdir – make directories

SYNOPSIS
     mkdir [-pv] [-m mode] directory_name ...

DESCRIPTION
     The mkdir utility creates the directories named as operands, in the order specified, using mode “rwxrwxrwx” (0777) as modified by the current
     umask(2).

     The options are as follows:

     -m mode        Set the file permission bits of the final created directory to the specified mode.  The mode argument can be in any of the formats
                    specified to the chmod(1) command.  If a symbolic mode is specified, the operation characters ‘+’ and ‘-’ are interpreted relative to
                    an initial mode of “a=rwx”.

     -p             Create intermediate directories as required.  If this option is not specified, the full path prefix of each operand must already exist.
                    On the other hand, with this option specified, no error will be reported if a directory given as an operand already exists.
                    Intermediate directories are created with permission bits of “rwxrwxrwx” (0777) as modified by the current umask, plus write and search
                    permission for the owner.

     -v             Be verbose when creating directories, listing them as they are created.

     The user must have write permission in the parent directory.

EXIT STATUS
     The mkdir utility exits 0 on success, and >0 if an error occurs.

EXAMPLES
     Create a directory named foobar:

           $ mkdir foobar

     Create a directory named foobar and set its file mode to 700:

           $ mkdir -m 700 foobar

     Create a directory named cow/horse/monkey, creating any non-existent intermediate directories as necessary:

           $ mkdir -p cow/horse/monkey

COMPATIBILITY
     The -v option is non-standard and its use in scripts is not recommended.

SEE ALSO
     rmdir(1)

STANDARDS
     The mkdir utility is expected to be IEEE Std 1003.2 (“POSIX.2”) compatible.

HISTORY
     A mkdir command appeared in Version 1 AT&T UNIX.
macOS 26.1                                                             March 15, 2013                                                            macOS 26.1
(END)

Explanation:

The -p option allows creation of parent directories if they do not exist and prevents errors when the directory already exists.

Screenshot:
<img width="1134" height="835" alt="Screenshot 2026-01-05 at 11 02 11 PM" src="https://github.com/user-attachments/assets/f12d0ce0-c452-4a94-8fce-767c33bc6a8f" />

6. Home Directory Inspection

Commands:

ls ~ | sort

Output:

Applications
Desktop
Documents
Downloads
Library
Movies
Music
Pictures
Public

Explanation:

This command lists all contents of the home directory and sorts them alphabetically for easier inspection

Screenshot:
<img width="750" height="175" alt="Screenshot 2026-01-05 at 11 05 26 PM" src="https://github.com/user-attachments/assets/6255510a-38f3-467f-90e7-87277cbe857c" />

7. Log Investigation

Commands:

echo "admin logged in" > log.txt

echo "user activity recorded" >> log.txt

grep "admin" log.txt

Output:

admin logged in

Explanation:

The grep command searches for the word “admin” inside the log file and displays only the matching lines.

Screenshot:<img width="565" height="81" alt="Screenshot 2026-01-05 at 11 08 57 PM" src="https://github.com/user-attachments/assets/866963ad-7428-49aa-926b-2358390dc2de" />

8. System Information Check

Commands:

uname -r

Output:

25.1.0

Explanation:

The uname -r command displays the version of the currently running Linux kernel.

Screenshot:
<img width="433" height="50" alt="Screenshot 2026-01-05 at 11 10 17 PM" src="https://github.com/user-attachments/assets/57a1f803-fd98-4ddf-9bf3-ea79cc23ed05" />

9. Network Connectivity Check

Commands:

ping -c 4 www.google.com

Output:

PING www.google.com (172.217.26.36): 56 data bytes
64 bytes from 172.217.26.36: icmp_seq=0 ttl=118 time=18.955 ms
64 bytes from 172.217.26.36: icmp_seq=1 ttl=118 time=31.091 ms
64 bytes from 172.217.26.36: icmp_seq=2 ttl=118 time=24.837 ms
64 bytes from 172.217.26.36: icmp_seq=3 ttl=118 time=19.607 ms

--- www.google.com ping statistics ---
4 packets transmitted, 4 packets received, 0.0% packet loss
round-trip min/avg/max/stddev = 18.955/23.622/31.091/4.878 ms

Explanation:

This command sends ICMP packets to Google to verify network connectivity. Successful replies confirm internet access.

Screenshot:<img width="527" height="156" alt="Screenshot 2026-01-05 at 11 11 54 PM" src="https://github.com/user-attachments/assets/89388816-baf2-45a1-b98d-27d52771db15" />


10. System Health Awareness

Command:

uptime

Output:

23:13  up 32 days, 11:28, 1 user, load averages: 1.67 2.48 3.10

Explanation:

The uptime command shows how long the system has been running, the number of logged-in users, and the load average, indicating overall system health.

Screenshot:
<img width="494" height="60" alt="Screenshot 2026-01-05 at 11 14 18 PM" src="https://github.com/user-attachments/assets/c0c34840-cde4-4a12-8d10-ae5a26fce3f4" />


