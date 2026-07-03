# Question 3: Explanations & Observations

* **Command:** `touch original_file.txt` & `echo "Hello Linux" > original_file.txt`
    * **Explanation:** I created a base text file and wrote the string "Hello Linux" into it to serve as the target for our linking experiment.
* **Command:** `ln original_file.txt hard_link.txt`
    * **Explanation:** I created a hard link to the original file. This acts as an additional physical name for the same underlying data block on the disk.
* **Command:** `ln -s original_file.txt sym_link.txt`
    * **Explanation:** I used the `-s` flag to create a symbolic (soft) link. This creates a pointer to the original file's location, rather than the data itself.
* **Command:** `ls -li original_file.txt hard_link.txt sym_link.txt`
    * **Explanation:** I listed the files displaying their inode numbers (`-i`). I observed that the original and hard link shared the same inode (3932608), while the symlink had a unique one (3932609).
* **Command:** `rm original_file.txt`
    * **Explanation:** I deleted the original source file to observe how the two different link types react to the target's removal.
* **Command:** `cat hard_link.txt` & `cat sym_link.txt`
    * **Explanation:** I attempted to read both links after deletion. The hard link successfully outputted "Hello Linux", while the symlink failed with a missing file error, proving soft links break when their target path is gone.