# sorta
Get rid of clutter in your directories. Sorta organizes your files by moving them to different folders based on their filetype and extensions.

We tend to download files on our PC's very often and usually this tends to pile up and before you know it, your downloads folder turns into a messy room. Or, you might just like to be organized and have a nice looking desktop. Sorta will take care of this for you by moving your notes, documents, music, images and videos into categorized folders.

It then takes this a step further by creating subfolders that stores files with the same extension.

## Installation
```bash
$ pip install sorta
```
<br>

### Usage
**Basic (Organizes your Desktop, Documents and Download directories)**
```bash
$ sorta
```
<br>

**Clean up a single specified directory. By default, sorta groups files by their filetype, but can group files by their category(see below).**
```bash
$ sorta -d /path/to/directory
```
<br>

### By category
By default, sorta groups your files by their filetype. You can choose to organize them by categories by using the command line flags '-c' or '--category'. You will have to create your own categories by using the '-ac' or '--addcategory' flags. These categories contain keywords or phrases that you would specifiy. It is best to make each keyword/key phrase as descriptive as possible. If a keyword/phrase was found in a filename, the file will be moved to the corresponding category folder.

**Organize your files in (documents,desktop and downloads) by category. **
```bash
$ sorta -c
```

<br>

**Organize your files in a specific directory by category.**
```bash
$ sorta -d /path/to/directory -c
```

### Allow sorta to run at intervals
**Note: In order to run Sorta in the background, you'll have to run a daemon command or your system's equivalent with Sorta along with the specified arguments(see below) as the process).**
Here is an example of running Sorta indefinitely, allowing it to clean up your directories periodically every 15 minutes. You can stop this by pressing Ctrl+c.
```bash
$ sorta -b -i 15
```

<br>
<br>

## Command Line Arguments
```text
usage: sorta [-h] [-b] [-d] [-i] [-c] [-ac]

Sorta, organize your filesystem. Running sorta without arguments organizes
your files in (documents,desktop, and downloads) by their filetype.

optional arguments:
  -h, --help          show this help message and exit
  -b, --background    Runs sorta indefinitely.
  -d , --directory    The directory you want to run sorta on.
  -i , --interval     How frequently you want sorta to run, in minutes.
  -c, --category      Sort files by category.
  -ac, --addcategory  Add or update an existing category to group files by.
```
