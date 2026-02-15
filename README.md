1. Launch this command, then Record its Job ID
	cat /dev/zero > /dev/null &

	[1] 24924

2. Use a single command to display detailed information about this process.
	ps -fp 24924

3. Save the full output of this command to a file named process_info.txt
	ps -fp 24924 > process_info.txt

4. Change the priority of this cat process between 10 and 15
	renice 12 -p 24924

5. Verify the change by displaying the process's new niceness value. Append this verification output to process_info.txt
	ps -o pid,ni,comm -p 24924 >> process_info.txt

6. Terminate the original cat /dev/zero > /dev/null process using its PID.
	kill 24924

7. Verify the process is no longer running.
	ps -p 24924
