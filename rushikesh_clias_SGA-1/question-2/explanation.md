# Question 2: Explanations & Observations

* **Command:** `umask`
    * **Explanation:** I checked the current system umask value, which returned `0002`. This determines the default permissions assigned to newly created files and directories.
* **Command:** `mkdir -p project_workspace/docs project_workspace/code`
    * **Explanation:** I used the `-p` flag to create a nested directory structure in one go. This successfully created the `project_workspace` parent folder and its `docs` and `code` subdirectories.
* **Command:** `touch project_workspace/docs/design.txt`
    * **Explanation:** I created a new empty text file named `design.txt` within the `docs` folder to test default file permissions.
* **Command:** `ls -l project_workspace/docs/design.txt`
    * **Explanation:** I viewed the long format listing of the file to check its permissions. It inherited `-rw-rw-r--`, which correctly reflects the 0002 umask applied to standard file permissions (666 - 002 = 664) for the user `rushikesh`.
* **Command:** `chmod 700 project_workspace/code`
    * **Explanation:** I restricted access to the `code` directory by changing its permissions to 700. This grants read, write, and execute permissions exclusively to the owner, securing the workspace.
* **Command:** `chown $USER:$USER project_workspace/docs/design.txt`
    * **Explanation:** I explicitly set the ownership of `design.txt` to the current user (`rushikesh`) and primary group to ensure proper ownership controls were in place.