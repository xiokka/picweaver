# picweaver

## Description
Static image gallery site generator written in Rust.
Generate simple image galleries.

## Usage

### Create new gallery
```bash
picweaver new_project $project_name
```
This will generate some basic project files and directories.

projectname.txt => contains project name.

static/base.html => base HTML file that will be used as a template to generate all pages. It contains two placeholders ($TITLE and $CONTENT) which the generator function will replace accordingly.

static/about.html => The $CONTENT of the homepage. This also contains the placeholder $NAVCLOUD, which the generator function will replace with links to each tag index page (each tag index page contains links to all entries for that tag).

entries/ => contains gallery entries.


### Create new gallery entry
```bash
picweaver new_entry $entry_name
```
Once a new entry is created, the corresponding subdirectory is created inside the entries directory. Within that entry, you will find two files ("tags.txt" and "content.html") and a subdirectory ("images/"). 

tags.txt contains the tags for that entry, where each tag is separated by a whitespace.

content.html is the gallery entry itself. It contains a placeholder $CONTENT which will be replaced with the images for that entry.

images/ contains all the images for that entry. Just dump them all in that directory and the generator function will insert them accordingly.

### Generate site
```bash
picweaver generate
```

This will create the public/ directory, where the site has been generated.
