# FileOrganizer
Console app to organize files from a target folder into an easy to navigate folder structure.

# Usage
FileOrganizer [options] in=[path of folder containing files to organize] out=[path of folder to construct organized structure in]

Options:
  -h, --help         Show this message and exit.
  -r, --recursive    Include files within subfolders of the 'in' folder.
                       NOTE: The folder structure of the 'in' folder is not reflected in the organized 'out' folder.
  -c, --copy         Only copy over the files from the 'in' folder and do not delete them.

Arguments:
  in=                The path (relative or absolute) to the folder containing the files to be organized.
  out=               The path (relative or absolute) to the folder where the organized folder structure will be constructed.
                       NOTE: If the top 'out' folder does not exist, it will be created.
                       NOTE: If the 'out' argument is not given, the organized structure will be created in the 'in' folder.

Examples:
  FileOrganizer in="~/Downloads" out="~/FileStorage"
  FileOrganizer -r -c in="/shares/sharedmedia" out="/home/jeff/SharedFiles"
  FileOrganizer in="/home/britta/documents"

# Organization Structure
By default, FileOrganizer creates the following folder structure as needed:
Documents
  - {year}
    - {month}
Media
  - Audio
    - {year}
      - {month}
  - Images
    - {year}
      - {month}
  - Books
    - {year}
      - {month}
  - Video
    - {year}
      - {month}
Software
  - {year}
    - {month}
Misc
