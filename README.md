一款基于QQ开放平台和Python-flask实现的冷笑话群聊机器人  
冷笑话来源60s.viki.moe 或 本地在线笑话库  
使用此系列程序可能需要提供以下参数: 
APP_ID  
CLIENT_SECRET （App Secret）  
BOT_SECRET     (Token)

需要特别注意的是QQ开放平台的回调设置需要使用https，故本程序仅可供已经有机构签发的（即含.key, .pem or .crt）SSL证书的域名使用  
请更改在配置区的SSL_CERT_PATH 和 SSL_KEY_PATH 为对应文件所在地址Windows系统r"C:...."
  
  
使用方法：  
零、准备工作：安装完整flask requests pynacl；指令为：pip install flask requests pynacl  ,开放8080 TCP 入方向端口  
一、回调设置：
请先在QQ开放平台-QQ机器人-开放-回调设置中配置事件回调地址并开启群事件中的“群消息事件AT事件”和“群打开消息推送”  
下载代码仓库中的“原始回调.py”修改对应信息，运行程序，在请求地址处输入 你的域名:8080/qq/callback，完成配置  
二、程序执行:  
“v1.0正式版.py” 本地笑话获取，此版本机器人指令为:/help, /讲个冷笑话, /添加冷笑话, /笑话统计  
如需运行此版本请下载“v1.0正式版.py”，“jokes.json”
“v1.1正式版.py” 在线笑话获取，此版本机器人指令为:/help, /讲个冷笑话, /更新公告  
如需运行此版本请下载“v1.1正式版.py”，本版本的本地笑话列表及更新公告需填写在“v1.1正式版.py”的对应区域中  

若增减功能请按照程序内的注释进行对应操作及更改
