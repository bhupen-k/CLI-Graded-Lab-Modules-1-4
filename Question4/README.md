1. System Uptime Verification:

Command:

uptime

OUtput:

 0:10  up 32 days, 12:25, 1 user, load averages: 1.60 2.47 2.71

 Explanation:

The uptime command shows how long the system has been running since the last boot along with load averages.

Screenshot:
<img width="566" height="72" alt="Screenshot 2026-01-06 at 12 11 13 AM" src="https://github.com/user-attachments/assets/cbae8db1-6a07-4252-8863-9ad3043d0422" />

2. User Process Listing

Command:

ps -u $(whoami)

Output (shown in screenshot)

Explanation:

This command lists all processes currently running under my user account.

Screenshot:
<img width="1135" height="831" alt="Screenshot 2026-01-06 at 12 12 55 AM" src="https://github.com/user-attachments/assets/0b5f132d-c7a1-4405-a8c2-3a31409693eb" />

3. CPU Usage Analysis

Command:

top -o %CPU

Output:

invalid argument -o: %CPU
top usage: top
                [-a | -d | -e | -c <mode>]
                [-F | -f]
                [-h]
                [-i <interval>]
                [-l <samples>]
                [-ncols <columns>]
                [-o <key>] [-O <secondaryKey>]
                        keys: pid (default), command, cpu, cpu_me, cpu_others, csw,
                                time, threads, ports, mregion, mem, rprvt, purg, vsize, vprvt,
                                kprvt, kshrd, pgrp, ppid, state, uid, wq, faults, cow, user,
                                msgsent, msgrecv, sysbsd, sysmach, pageins, boosts, instrs, cycles
                [-R | -r]
                [-S]
                [-s <delay>]
                [-n <nprocs>]
                [-stats <key(s)>]
                [-pid <processid>]
                [-user <username>]
                [-U <username>]
                [-u]
                [-W]

Explanation:

The top command displays real-time process information. Sorting by CPU usage helps identify the process consuming the most CPU resources.

Screenshot:
<img width="786" height="344" alt="Screenshot 2026-01-06 at 12 15 34 AM" src="https://github.com/user-attachments/assets/8c17a8ae-b91c-45df-95ec-2cec992e6d82" />

4. Background Process Execution

Command:

sleep 300 &
jobs

Output:

[1] 20148
[1]  + running    sleep 300

Explanation:

The sleep command was executed in the background using &. The jobs command confirms that the background process is running.

Screenshot:
<img width="472" height="111" alt="Screenshot 2026-01-06 at 12 16 54 AM" src="https://github.com/user-attachments/assets/91fa3f11-1ec6-4236-9daa-cee283031109" />

5. Process Priority Management

Commands:

ps -o pid,ni,comm -u $(whoami)
renice 10 -p <PID>

Explanation:

The renice command changes the priority (niceness) of a running process. Increasing the niceness lowers the process priority.

6. Memory Usage Monitoring

Commands:

vm_stat

Output:

Mach Virtual Memory Statistics: (page size of 16384 bytes)
Pages free:                                4337.
Pages active:                            105685.
Pages inactive:                           94309.
Pages speculative:                         1606.
Pages throttled:                              0.
Pages wired down:                        115653.
Pages purgeable:                            694.
"Translation faults":                5845718072.
Pages copy-on-write:                   67319769.
Pages zero filled:                   1611154638.
Pages reactivated:                   1318249525.
Pages purged:                         327359379.
File-backed pages:                        54008.
Anonymous pages:                         147592.
Pages stored in compressor:              825749.
Pages occupied by compressor:            166864.
Decompressions:                      2716612649.
Compressions:                        3074232060.
Pageins:                              248956911.
Pageouts:                               4051990.
Swapins:                              143651836.
Swapouts:                             148036129.

Explanation:

This command displays memory usage statistics, showing how system memory is allocated and used.

Screenshot:
<img width="573" height="394" alt="Screenshot 2026-01-06 at 12 20 28 AM" src="https://github.com/user-attachments/assets/8b27639c-a5c8-4760-bcd5-44ed5a3c831f" />

7. Disk Space Inspection

Commands:

df -h ~

OUtput:

Filesystem      Size    Used   Avail Capacity iused ifree %iused  Mounted on
/dev/disk3s5   228Gi   134Gi    70Gi    66%    942k  732M    0%   /System/Volumes/Data
bhupen@Bhupens-MacBook-Air ~ % 
[1]  + done       sleep 300

Explanation:

The df -h command displays disk space usage of the filesystem where the home directory resides in a human-readable format.

Screenshot:
<img width="726" height="146" alt="Screenshot 2026-01-06 at 12 21 47 AM" src="https://github.com/user-attachments/assets/c9daf9cf-e8a0-4316-bcc4-de9e9edc9faf" />

8. Shell Identification

Commands:

echo $SHELL

Output:

/bin/zsh

Explanation:

This command displays the name of the shell currently in use.

Screenshot:
<img width="414" height="71" alt="Screenshot 2026-01-06 at 12 23 01 AM" src="https://github.com/user-attachments/assets/b1ab19f4-8e2a-4ad4-b9b5-bcb5708e4e3b" />

9. Output Redirection

Command:

uname -a > system_report.txt
cat system_report.txt

Output:

Darwin Bhupens-MacBook-Air.local 25.1.0 Darwin Kernel Version 25.1.0: Mon Oct 20 19:32:47 PDT 2025; root:xnu-12377.41.6~2/RELEASE_ARM64_T8103 arm64

Explanation:

The output of the system information command is redirected into a file named system_report.txt using output redirection.

Screenshot:<img width="1084" height="78" alt="Screenshot 2026-01-06 at 12 25 04 AM" src="https://github.com/user-attachments/assets/50c96ac1-6f8a-4ef6-a4ab-4484f475fe7f" />

10. Disk Usage Visualization (`ncdu`)

Command:

ncdu ~

Output:
ncdu 2.9.2 ~ Use the arrow keys to navigate, press ? for help                                                                                                
--- /Users/bhupen -------------------------------------------------------------------------------------------------------------------------------------------
.  21.3 GiB [######################] /Library                                                                                                                
   14.5 GiB [##############        ] /Documents
    9.6 GiB [#########             ] /Downloads
    1.2 GiB [#                     ] /.vscode
    1.1 GiB [#                     ] /Movies
  415.4 MiB [                      ] /Desktop
. 187.4 MiB [                      ] /Pictures
  109.6 MiB [                      ] /.config
   42.4 MiB [                      ] /Music
   11.7 MiB [                      ] /Applications
   96.0 KiB [                      ] /.codex
   28.0 KiB [                      ]  .DS_Store
   20.0 KiB [                      ] /.zsh_sessions
   16.0 KiB [                      ] /.local
    8.0 KiB [                      ] /.android
    4.0 KiB [                      ]  .zsh_history
    4.0 KiB [                      ] /.mono
    4.0 KiB [                      ]  .zprofile
    4.0 KiB [                      ]  system_report.txt
    4.0 KiB [                      ] /.redhat
    4.0 KiB [                      ]  .zshrc
H   4.0 KiB [                      ]  sample_hard.txt
H   4.0 KiB [                      ]  sample_data.txt
    4.0 KiB [                      ]  .lesshst
    4.0 KiB [                      ]  .CFUserTextEncoding
    0.0   B [                      ] /Public
!   0.0   B [                      ] /.Trash


Explanation:

The ncdu tool provides an interactive view of disk usage, making it easier to identify directories consuming the most space.

Screenshot:
<img width="1136" height="833" alt="Screenshot 2026-01-06 at 12 29 03 AM" src="https://github.com/user-attachments/assets/0e21f679-f9a6-4163-b271-a59eab7120dd" />

