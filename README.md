# socfire

SocFire Instructions:

1) sudo apt-get install python3-pip
2) sudo pip3 install selenium
3) sudo pip3 install pandas
4) sudo apt-get install python3-dev libxml2-dev libxslt1-dev zlib1g-dev
5) sudo3 pip install lxml
6) sudo pip3 install xvfbwrapper

Add a text file with a list of IP addresses from Security Events, name it "IP.txt" put it in the same directory as socfire.py

Add the list of keywords to "keyword_list.txt" and keep it in the same directory of socfire.py

Usage: "sudo python3 socfire.py"

Let it run through the errors, it will output a file called "results.csv" with the results of the google searches.  I recommind filtering each column.  After a few searches your eyes will be trained to look for anomalies.  After running the file, remove the results.csv file as the new search will overwrite.

There a number of use cases:

1.  Export a list of all hosts communicating with High-Risk Countries, and run the destination IP addresses through this search to determine if any of them are linked with malicious behavior.

2.  Export a list of source IP addresses that have triggered security events.  Run the source IP addresses through this search to determine if any of these are linked to malware campaigns or other indicators that it might be a persistant targeted attack.

3.  Export a list of all IP addresses a known infected host was communicating with to determine if there are any other indicators that would signify further compromise.

4.  Export a list of high bandwidth usage for hosts transferring data to determine if any of the IP addresses can be linked to threat actors.
