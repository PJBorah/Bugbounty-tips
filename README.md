# Bugbounty-tips
All My oneline


subs dns brute:
ffuf -u "https://FUZZ.sdge.com" -w /home/cyb3r/CYBER/wordlist/SecLists-master/Discovery/DNS/subdomains-top1million-20000.txt -mc 200,403,404,302,301 

find urls from all the domain subs list:
waybackurls /home/cyb3r/Desktop/bug/zuora/1 >> ul    

after collecting all the urls uisng waybackmachine only need parameters and also remove duplicate parameters:
cat urls.txt | sed -n 's/.*?\(.*\)/\1/p' | tr '&' '\n' | awk -F= '!seen[$1]++'
