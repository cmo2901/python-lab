# Updating a File with Python

## Objective
<p> In this project, I utilize a python script to update a file of IP addresses that have access to restricted content. I achieved this by iterating through a list of IP addresses that must be removed from the allow list.</p>

### Tools Used
<p> Python <br>
Jupyter Notebooks</p>

### Opening and reading the allow list
<p> After importing the file into Python, I needed to open it and read the contents. I started by opening the file with the 'r' parameter, then storing 'file.read()' into a variable named 'ip_addresses.' I then used a simple print statement to display the file's contents. </p>

<img width="750" alt="Open and read file contents" src="https://github.com/user-attachments/assets/75dda15b-cb25-4081-9192-a339bb6273c7" />

### Converting the string into a list
<p>Since the goal of my program was to remove individual elements from a file, I needed to convert it to a list using the .split() method.</p>

<img width="766" alt="Convert file from string to list" src="https://github.com/user-attachments/assets/253722b8-fed0-4b82-85d2-9d58b2f4cb7a" />

### Iterating through the remove list
<p>From here, I built a for loop that would iterate over the remove list to check which elements were contained in the allow list. A conditional statement would pass the element as an argument into the .remove() method to remove it from the allow list. It was possible to do it this way because the allow list file did not contain any duplicate IP addresses.</p>

<img width="620" alt="Iterate through remove list" src="https://github.com/user-attachments/assets/1f85313b-5618-449a-9c20-3303c6573498" />

### Updating the original file
<p>With the unauthorized IP addresses removed from the file, I could now update it. First, I converted the file from a list back to a string with the .join() method, and utilized '\n' to give each element of the updated file its own line. By storing '.join(ip_addresses)' in the 'ip_addresses' variable, I could pass this variable as an argument when replacing the original file's contents. Using a print statement, I confirmed that the updated file excluded any elements from the remove list.</p>

<img width="518" alt="Update the original file" src="https://github.com/user-attachments/assets/3456190d-c721-4275-b885-04e472192c35" />
