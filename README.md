##### PAPI-Google (Pydrive Wrapper)
Python API for Google - This makes life a lot easier than the vanilla api commands


###The Functions and their Parameters:
## Exploring the Filesystem
# List Files in Directory (By id)
`list_drive_directory(id=None)`


NOTE: The below functions have a "files" parameter - this can be retrieved using `list_drive_directory`

# Check for matching title in folder 
`check_files_for_title(files=None,title=None)`

# Check for matching id in folder
`check_files_for_id(files=None,id=None)`

# Get titles from filelist
`get_titles_from_fileList(fileList)`

# Get mimetypes from filelist
`get_mimes_from_fileList(fileList)`

# Get ids from filelist
`get_ids_from_fileList(fileList)`


# Query Drive
Note: This is the same thing as the normal api calls, except the result is extremely streamlined - For more detail, use the `get_drive_file` function instead
`query_drive(query)`

## Downloading Files
# Download all files in a directory (via id)
`download_drive_dir_files(id=None)`


# Download file via id
`download_drive_file(id=None, file_name=None, directory=None)`


## Creating Files
# Create a Folder (with parent id)
`create_drive_folder(parent_id=None, title=None)`

# Create a Document
`create_drive_document(title=None, parent_id=None)`

# Create a Document from a Template
`create_document_from_template(template_id=None, batch_update=None, target_directory=None, file_title=None)`




## Deleting Files
Disclaimer: I have no idea why, but deleting a file on it's own is proving difficult. Deletion of folders works out just fine however

# Delete a Folder (via id):
`delete_drive_folder(id=None)`


# Trash a Folder (via id):
`trash_drive_folder(id=None)`



## Copying & Moving Files
# Copy a File into another Folder
`copy_drive_file_to_folder(file_id=None, copy_title=None, parent_id=None)`

# Copy a File into the same Folder
`copy_drive_file(file_id=None, copy_title=None)`

# Move a File into another Folder
`move_drive_file(file_id=None, parent_id=None)`



## "Getting" Files
Note: this returns the file in the same format as the regular api
`get_drive_file(id=None)`



## Editing Files
# Rename Docs File
`rename_drive_document(id=None,title=None)`

# Insert text to document (hyperlinks supported)
`insert_text_to_drive_document(id=None, text=None, index=1, link=None, font="Anonymous Pro", font_size=30)`



## Uploading Files
# Upload a file to a folder
`upload_file_to_drive(file=None, directory=None, parent_id=None, file_name=None)`