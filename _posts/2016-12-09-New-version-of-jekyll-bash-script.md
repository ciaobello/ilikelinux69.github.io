---
layout: post
title: New version of jekyll bash script
date: 2016-12-09 19:30
---

Some changes to shorten und style the script.

``` 
#!/bin/bash
#set color ORANGE and NC.
ORANGE='\033[0;33m'
NC='\033[0m' # No Color 

# creates date as variable "jekyll_date" in form off (2016-12-2)
jekyll_date=$(date +"%F")
jekyll_date_time=$(date +"%F %H:%M")


# asks for title name to type in in terminal
echo -e ""${ORANGE} 
echo " ****************************************************"
echo " Enter title, exerp and blogtext in the fields below:"
echo -e " ****************************************************" ${NC}
echo -ne  " Title: "${ORANGE} & read title
echo -e "" ${NC}
echo -ne  " Exerp: "${ORANGE} & read exerp
echo -e "" ${NC}
echo -ne  " Blogtext: "${ORANGE} & read blog_text
echo -e "" ${NC}
echo ""

# substitutes blanks in title with dashes und writes it to new variable
file_name="$jekyll_date-${title// /-}"


read -p " Press [Enter] to create the blogentry or abort with [CTRL]&[C]..."


# creates a file with the syntax of jekyll

> "$file_name.md"

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
