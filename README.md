awk -F',' '$1 ~ /^16:17/ { print }' logfile.csv > time.csv
cat time.csv
we get all 16:17 om the page
---------
awk -F',' '$2 != "INFO" time.csv > noinfo.csv
cat noinfo.csv
we put all the lines exept the lines that have info to the noinfo file
------------
cat noinfo.csv | grep WARN | wc -l
tells us how many warns we have
-----------
awk -F',' '{print $3}' noinfo.csv | sort -u
tells us all the class names
