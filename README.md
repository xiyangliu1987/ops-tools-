ops-tools

项目中代码为日常工作中，积累下来的脚本。

extmail
公司规模较小的时候，使用了开源的电子邮箱服务器。
使用postfix、maildrop、dovecot等开源组件搭建了电子邮箱的后台。
使用extmail作为webmail来对用户提供网页访问。
在使用初期，由于缺乏经验，没有有效的管理dspam特征库，造成用户收件夹垃圾邮件和正常的邮件混杂的问题，用户体验非常差。
管理员在后台替用户过滤一下。待初始化dspam的特征库后，经过一周的人工训练，基本可以达98%以上的识别率。
故写脚本，若用户要求，则自动对用户收件夹中的文件一一判断，自动移除垃圾邮件，为防止误杀，提供了恢复邮件的措施。

nagios2
nagios使用过程中，每一个主机需要生成一个配置文件。公司交换机数量达300余台。
维护这300余个配置文件就成了一个较大的麻烦。
故，写脚本将交换机根据huawei的h3c等不同的生产厂商，自动生成配置文件，并定期维护。

phpdisk
phpdisk是国内开源的简易网盘php程序。通过apache建站后，可提供web网盘服务。公司下属医院实现内外网隔离，又有医护人员传递文件的需求，故在一台双线服务器上搭建了此网盘服务。为了排除病毒和非法文件。使用file命令，检测每个上传的文件，只允许doc、ppt、jpg、txt等文件在服务器上存在。移除其余的文件。

