# Activity Overview

In this activity, you will demonstrate your experience using Python to develop algorithms that involve opening files and parsing their contents. 

## Scenario

You are a security professional working at a health care company. As part of your job, you're required to regularly update a file that identifies the employees who can access restricted content. The contents of the file are based on who is working with personal patient records. Employees are restricted access based on their IP address. There is an allow list for IP addresses permitted to sign into the restricted subnetwork. There's also a remove list that identifies which employees you must remove from this allow list.

Your task is to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, you should remove those IP addresses from the file containing the allow list.

---
## Python File Parsing — Update an IP Allow List

This report was completed as part of the Google Cybersecurity Certificate. It documents how to use Python to automate the process of updating a file that contains IP addresses authorized to access restricted healthcare data. These tasks are essential for access control, secure file handling, and foundational automation techniques in cybersecurity.

## My Contributions

- **Open the allow list file**
  - Assigned `"allow_list.txt"` to the `import_file` variable
  - Used a `with open(import_file, "r")` statement to safely access the file
  - Stored the file object in the variable `file` for use within the block

- **Read the file contents**
  - Applied `.read()` to extract the contents of the file as a single string
  - Stored the result in a variable named `ip_addresses`

- **Convert the string into a list**
  - Used `.split()` to transform the string into a list of individual IP addresses
  - This allowed for easier comparison and filtering

- **Iterate through the remove list**
  - Defined a `remove_list` containing IPs that should no longer have access
  - Used a `for` loop with `element` as the loop variable to iterate through `remove_list`

- **Remove IP addresses that are on the remove list**
  - Inside the loop, used an `if` statement to check if `element` was in `ip_addresses`
  - Applied `.remove(element)` to delete matching IPs from the allow list
  - This method worked safely because the allow list contained no duplicate entries

- **Update the file with the revised list of IP addresses**
  - Used `"\n".join(ip_addresses)` to convert the list back into a newline-separated string
  - Opened the file again using `with open(import_file, "w")` to overwrite its contents
  - Applied `.write()` to save the updated list back to the file
    
## Tools Used

- `open()` — to read and write files
- `.read()` — to extract file contents as a string
- `.split()` — to convert strings into lists
- `for` loop — to iterate through IPs flagged for removal
- `if` statement — to check for matches
- `.remove()` — to delete unauthorized IPs
- `.join()` — to format the updated list for file writing
  
## Reflections

- Wrapping the logic into a function made the code reusable for future access control tasks.
- Using `with open()` ensured safe file handling without manual closing.
- The `.split()` and `.join()` methods were essential for converting between string and list formats.
- Automating the removal of IPs from the allow list demonstrated how Python can streamline security operations.
- This algorithm could easily be adapted for other access control systems or log file audits.

---

## Screenshot of Updating A File A Through Python Algorithm
![Updating A File A Through Python Algorithm Snapshot](python.png)
> This image captures the full response submitted as part of the Google Cybersecurity Certificate Python Algorithm report activity.
> 
