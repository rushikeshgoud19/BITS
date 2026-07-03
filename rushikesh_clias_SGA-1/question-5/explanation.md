# Question 5: Explanations & Observations

* **Command:** `lsblk`
    * **Explanation:** I ran this command to list all available block storage devices. It identified the main 80.1G disk (`sda`) and its primary partition (`sda1`).
* **Command:** `df -h`
    * **Explanation:** I used this to display disk space usage in a human-readable format. I observed that the root partition (`/dev/sda1`) was only at 23% utilization, meaning there is ample space for new deployments.
* **Command:** `df -i`
    * **Explanation:** I checked the inode utilization to ensure we aren't running out of file index limits. The output showed only 10% inode usage on the root partition, indicating a very healthy file system.
* **Command:** `vi Storage_Assessment_Report.txt`
    * **Explanation:** I opened the `vi` text editor to compile my findings and recommendations into a formal storage health assessment document.