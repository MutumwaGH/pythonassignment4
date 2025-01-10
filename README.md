# pythonassignment4
# File Read and Write Challenge

    # Open the source file to read
    with open("source.txt", "r") as source_file:
        content = source_file.read()

    # Modify the content (e.g., convert to uppercase)
    modified_content = content.upper()

    # Write the modified content to a new file
    with open("modified.txt", "w") as modified_file:
        modified_file.write(modified_content)

    print("File has been read, modified, and written to 'modified.txt'.")
except FileNotFoundError:
    print("The source file 'source.txt' does not exist.")
except Exception as e:
    print(f"An unexpected error occurred: {e}")
    
# Error Handling Lab
filename = input("Enter the filename to read: ")

    # Attempt to open and read the file
    with open(filename, "r") as file:
        content = file.read()
        print("File content:")
        print(content)
except FileNotFoundError:
    print(f"Error: The file '{filename}' does not exist.")
except PermissionError:
    print(f"Error: You do not have permission to read '{filename}'.")
except Exception as e:
    print(f"An unexpected error occurred: {e}")
