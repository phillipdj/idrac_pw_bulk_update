iDRAC Password Bulk Update Script
This repository contains a Python script to automate the process of changing iDRAC passwords across multiple devices via SSH. The script reads a list of iDRAC IP addresses from an Excel file and updates the password for each device.

Features
Automated Password Change: The script connects to each iDRAC device using SSH and runs the necessary command to change the password.
Excel Integration: IP addresses of the iDRAC devices are read from an Excel file, simplifying the management of devices.
Error Handling: The script includes basic error handling, allowing it to skip devices that cannot be accessed or where the password change fails.
Prerequisites
Before running the script, ensure you have the following installed:

Python 3.x
Required Python packages: paramiko, pandas, openpyxl (for reading Excel files)
You can install the necessary packages using pip:

sh
Copy code
pip install paramiko pandas openpyxl
Usage
Prepare the Excel File: Create an Excel file (idrac_pw_bulk_update_ip_addresses.xlsx) with the following structure:

Sheet Name: IP Addresses (or change the sheet_name variable in the script)
Column Name: IP (or change the column_name variable in the script)
The column should contain the IP addresses of the iDRAC devices you want to update.

Update the Script:

New Password: Replace "New password here" with the new password you want to set.
Credentials: Replace "Username here" and "Old password here" with the current iDRAC username and password.
Run the Script:

sh
Copy code
python idrac_password_update.py
The script will iterate through the list of IP addresses from the Excel file and attempt to change the password on each iDRAC device.

Error Handling
The script will print an error message for any device where the password change fails, allowing you to diagnose and fix issues manually.

Debugging
To assist with debugging, the script provides console output that includes successful password changes as well as errors encountered during execution.

Contribution
Contributions are welcome! Feel free to fork this repository, submit pull requests, or open issues for any bugs or feature requests.

License
This project is licensed under the MIT License. See the LICENSE file for details.
