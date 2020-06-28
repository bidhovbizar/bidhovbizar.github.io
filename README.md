# bidhovbizar.github.io
Webpage creation

First Step
1. Connect to IISc VPN. 
2. https://digits.iisc.ac.in/iisc-vpn/
3. https://digits.iisc.ac.in/wp-content/uploads/2019/05/How_to_download_VPN.pdf
4. https://vpn.iisc.ac.in/+CSCOE+/logon.html#form_title_text 

Second Step : Create a public private key not typing password repeatedly
1. Create a public private key pair: https://docs.oracle.com/en/cloud/paas/database-dbaas-cloud/csdbi/generate-ssh-key-pair.html#GUID-4285B8CF-A228-4B89-9552-FE6446B5A673
2. Once create the public private key pair, connect to IISc VPN.  
3. scp ~/.ssh/id_rsa.pub username@ececloud.iisc.ac.in:~/web/
4. ssh username@ececloud.iisc.ac.in
5. Once logged in, go to your .ssh directory and save your public key there in authorized_keys file. 

Third Step : Create a webpage using jemdoc
1. Take help from Jemdoc page: https://jemdoc.jaboc.net/

OR 

1. git clone https://github.com/parimalparag/parimalparag.github.io
2. cp index.jemdoc, changWeb.sh, jemdoc.css, jemdoc.py, MENU, mysite.conf from parimalparag.github.io and copy to bidhovbizar.github.io 
3. chmod +x changeWeb.sh 
4. chmod +x jemdoc.py
4. ./changeWeb.sh //This will only work for python 2.7
5. scp index.html username@ececloud.iisc.ac.in:~/web/
