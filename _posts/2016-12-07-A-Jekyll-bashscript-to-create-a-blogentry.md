---
title: A Jekyll bashscript to create a blogentry
date: 2016-12-07 17:00:00 Z
layout: post
comments: true
---

Smal script to atomatize a Jekyll post in the terminal with bash.

The easyest way to use the script is, to create a
`mkdir /home/$USER/bin`{: style="color: red"} directory in your home drive. I named mine
`touch blogentry`{: style="color: red"}. Just dont forget to make it executable!

`chmod +x blogentry`{: style="color: red"} does the trick.

To copy the script content in to the file i like to use nano.
`nano blogentry`{: style="color: red"} would be the command.

```
#!/bin/bash

# creates variable "jekyll_date" in form off (2016-12-2)
jekyll_date=$(date +"%F")
jekyll_date_time=$(date +"%F %H:%M")

# prints the variable
echo "Jekyll_date: $jekyll_date $jekyll_dat_time"
echo ""

# asks for title name to type in in terminal
echo  " Please enter the title of your blog entry:";
echo  " ******************************************";
echo  ""

# shows prompt to type the variable in
read title 

# asks for exerp of the blog entry to type in in terminal
echo  " Please enter the exerp of your blog entry:";
echo  " __________________________________________";
echo ""
echo ""
# shows prompt to type the 'exerp' variable in
read exerp

# asks for the blog_text to type in in terminal
echo  " Please enter the blog_text of your blog entry:";
echo  " ______________________________________________";
echo ""
echo ""
# shows prompt to type the 'blog_text' variable in
read blog_text

# prints the two variables created above
echo " Shows the two variables (jekyll-date & title) created"
echo " ---------------------------------------------------"
echo " Jekyll_date: $jekyll_date; title: $title"

# substitutes the blanks in title 
#with dashes und writes it to new variable
file_name="$jekyll_date-${title// /-}"

# prints the new variable on the screen
echo " file_name: $jekyll_date-${title// /-}"

# creates a file with the syntax of jekyll
> "$file_name.md"

# creaing the front matter, exerp & blog-text
echo "---" >> "$file_name.md"
echo "layout: post" >> "$file_name.md"
echo "title: $title" >> "$file_name.md"
echo "date: $jekyll_date_time" >> "$file_name.md"
echo "---" >> "$file_name.md"
echo "" >> "$file_name.md"
echo "$exerp" >> "$file_name.md"
echo "" >> "$file_name.md"
echo "$blog_text" >> "$file_name.md"
echo "" >> "$file_name.md"


nano "$file_name.md"

```

