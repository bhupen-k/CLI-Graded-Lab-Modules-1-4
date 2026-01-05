1. Project Workspace Setup

Command:

mkdir ~/documents

Output:

mkdir: /Users/bhupen/documents: File exists

Explanation:

This command creates a directory named documents inside my home directory to store project-related files.

Screenshot:
<img width="474" height="65" alt="Screenshot 2026-01-05 at 11 21 28 PM" src="https://github.com/user-attachments/assets/43697da6-331f-4118-8246-f1bd80d3a075" />

2. File Creation

Commands:

cd ~/documents

touch plan.txt

Output: (File is created which is circled in the screenshot)

Explanation:

I navigated into the documents directory and created an empty file named plan.txt

Screenshot:
<img width="793" height="722" alt="Screenshot 2026-01-05 at 11 23 40 PM" src="https://github.com/user-attachments/assets/50d35944-9731-49c4-90bc-501982fce2a5" />

3. Content Addition

Commands:

echo "This is a sample project plan file." > plan.txt

cat plan.txt

Output: (Content is added to file)

This is a sample project plan file.

Explanation:

This command writes sample text into the plan.txt file and verifies the content using the cat command.

Screenshot:
<img width="677" height="43" alt="Screenshot 2026-01-05 at 11 30 30 PM" src="https://github.com/user-attachments/assets/d806e81a-7ca7-4718-9291-7a23ecb81b8d" />


4. File Metadata Verification

Commands:

ls -l plan.txt

Output:

-rw-r--r--  1 bhupen  staff  36 Jan  5 23:27 plan.txt

Explanation:

The ls -l command displays file permissions, ownership, and size, confirming that the file belongs to my user account.

Screenshot:
<img width="491" height="69" alt="Screenshot 2026-01-05 at 11 30 10 PM" src="https://github.com/user-attachments/assets/cf0a8976-88f9-4ebb-aba8-61e1b08ec954" />

5. File Duplication

Commands:

cp plan.txt plan_copy.txt

Output: (The duplicate file is created with name plan_copy.txt)

Explanation:

This command creates a duplicate of plan.txt named plan_copy.txt.

Screenshot:
<img width="976" height="563" alt="Screenshot 2026-01-05 at 11 32 42 PM" src="https://github.com/user-attachments/assets/df3d8c4f-5287-4ae5-9801-cf74d41f0323" />

6. Directory Renaming

Commands:

mv documents project_documents

Output:

mv: rename documents to project_documents: Permission denied

Explanation:

This command renames the documents directory to project_documents to better reflect its purpose.

Screenshot:
<img width="504" height="98" alt="Screenshot 2026-01-05 at 11 35 04 PM" src="https://github.com/user-attachments/assets/e1800f70-22e8-4a26-a3bb-0db7c8c8d264" />

7. Archival Structure:

Commands:

mkdir ~/project_documents/archive

Output: (This is because renaming was denied in previous task)

mkdir: /Users/bhupen/project_documents: No such file or directory

Explanation:

This command creates a subdirectory named archive inside project_documents for storing older files.

Screenshot:

<img width="523" height="58" alt="Screenshot 2026-01-05 at 11 36 48 PM" src="https://github.com/user-attachments/assets/9b29b6ce-613b-453e-b160-3f1dbbbd9091" />

8. File Organization

Commands:

mv ~/project_documents/plan_copy.txt ~/project_documents/archive/

Outputs: (Because renaming was denied in previous task)

mv: rename /Users/bhupen/project_documents/plan_copy.txt to /Users/bhupen/project_documents/archive/: No such file or directory

Explanation:

This command moves the copied file into the archive subdirectory to organize project files.

Screenshot:
<img width="994" height="84" alt="Screenshot 2026-01-05 at 11 38 31 PM" src="https://github.com/user-attachments/assets/13a0500f-7489-4eb1-97e7-87fa0d8eb281" />

9. Recursive Listing

Commands:

ls -R ~/project_documents

OUtput: (Because renaming was denied)

ls: /Users/bhupen/project_documents: No such file or directory

Explanation:

The -R option lists all files and subdirectories recursively, showing the complete directory structure.

Screenshot:

<img width="738" height="110" alt="Screenshot 2026-01-05 at 11 39 59 PM" src="https://github.com/user-attachments/assets/9edff69f-6563-4931-8663-fe7141cd17b3" />

10. Path Verification

Commands:

realpath ~/project_documents/archive/plan_copy.txt

Output:

realpath: /Users/bhupen/project_documents/archive/plan_copy.txt: No such file or directory

Explanation:

This command displays the absolute path of the file after it was moved, confirming its final location.

Screenshot:
<img width="718" height="54" alt="Screenshot 2026-01-05 at 11 41 46 PM" src="https://github.com/user-attachments/assets/af65d080-c122-485c-8281-b7f76ed27b68" />


