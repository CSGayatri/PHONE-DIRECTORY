# 📇 Contact Directory using Trie in C++

This is a console-based **Contact Directory** built using **Trie data structure** in C++. It allows you to store, search, and delete contact records efficiently based on either the person's **name** or **phone number**.

## 🔧 Features

- ➕ **Add Contact**: Stores contact details (Name, Phone Number, ID, Start Date).
- 🔍 **Search Contact**: Lookup by either name or phone number.
- ❌ **Delete Contact**: Remove a contact using the phone number.
- 📂 **Efficient Storage**: Uses Trie with 37 branches (0–9, A–Z, and space) for fast operations.

## 🧩 Data Structure

Each node in the Trie contains:
- An array of 37 links (`A-Z`, `0-9`, space).
- A vector of `Data` structs representing contact records at the node.

```cpp
struct Data {
    string phone_number;
    string name;
    string ID;
    string start_date;
};
📌 How It Works
Insert: Inserts the record in two tries — one for the name and one for the phone number.

Search: Traverses the Trie based on user input and collects all matching records.

Delete: Clears the vector at the phone number path and removes the corresponding entry in the name Trie.
🧪 Usage
Run the program and follow the menu:

pgsql
Copy
Edit
WELCOME TO THE DIRECTORY!!!!

FOR ADDING DATA: TYPE 1
FOR ACCESSING INFORMATION: TYPE 2
FOR ERASING DATA: TYPE 3
FOR AN EXIT: TYPE 4

Input Format
Name (can include spaces)

Phone Number (digits only)

ID (any string)

Start Date (any format)

Example
yaml
Copy
Edit
ENTER YOUR CHOICE:
1
ENTER THE NAME: John Doe
ENTER THE PHONE NUMBER: 9876543210
ENTER THE ID: A102
ENTER THE START DATE: 2023-06-01

🛠 Compilation & Execution
📌 Using g++
bash
Copy
Edit
g++ -o directory directory.cpp
./directory

🚀 **Future Enhancements**
File-based persistent storage
GUI Interface
Support for advanced search filters (e.g., date range)
Sorting of displayed data

