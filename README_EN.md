Here is the English translation maintaining the original context and preserving filenames in quotes:

A cold joke group chat bot implemented based on the QQ Open Platform and Python-Flask  
Cold joke sources: 60s.viki.moe or local joke database  

Using this series of programs may require providing the following parameters:  
APP_ID  
CLIENT_SECRET (App Secret)  
BOT_SECRET (Token)  

Special note: The QQ Open Platform callback settings require HTTPS. Therefore, this program can only be used with domains that already possess institution-issued SSL certificates (i.e., containing .key, .pem or .crt files).  
Please modify SSL_CERT_PATH and SSL_KEY_PATH in the configuration section to the corresponding file locations. Windows system example: r"C:...."  

Usage:  
0. Preparations: Install flask, requests, and pynacl. Command:  
   pip install flask requests pynacl  
   Open TCP port 8080 for inbound connections.  

1. Callback Setup:  
   First, configure the event callback address in QQ Open Platform > QQ Bot > Open Platform > Callback Settings. Enable "Group Message Events (@ Events)" and "Group Message Push" under group events.  
   Download "原始回调.py" from the code repository, modify the corresponding information, run the program, and enter your domain:8080/qq/callback in the request address field to complete the setup.  

2. Program Execution:  
   "v1.0正式版.py": Local joke retrieval. Commands for this version:  
   /help, /讲个冷笑话, /添加冷笑话, /笑话统计  
   To run this version, download "v1.0正式版.py" and "jokes.json".  

   "v1.1正式版.py": Online joke retrieval. Commands for this version:  
   /help, /讲个冷笑话, /更新公告  
   To run this version, download "v1.1正式版.py". The local joke list and update announcements for this version need to be filled in the corresponding sections of "v1.1正式版.py".  

If adding or removing features, please follow the instructions in the program comments for corresponding operations and modifications.
