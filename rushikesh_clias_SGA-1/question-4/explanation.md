# Question 4: Explanations & Observations

* **Command:** `ls /fake_directory > standard_out.txt 2> error_out.txt`
    * **Explanation:** I attempted to list a non-existent directory while redirecting standard output (FD 1) to `standard_out.txt` and standard error (FD 2) to `error_out.txt`. This demonstrates stream separation.
* **Command:** `cat error_out.txt`
    * **Explanation:** I read the contents of the error file and confirmed that the standard error message from the failed `ls` command was successfully trapped and logged here, proving the `2>` redirection worked.
* **Command:** `ulimit -a`
    * **Explanation:** I executed this to view the current shell's resource limits for my user profile. It provided a breakdown of system constraints, such as the maximum number of open files (1024) permitted.