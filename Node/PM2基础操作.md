一、简介
pm2是一个内置负载均衡的node.js应用进程管理器（也支持Windows）,其它的类似功能也有不少，但是感觉pm2功能更强
　使用体会：
　　1.简单易用、后台运行、快速部署，常用到的命令就几个
　　2.可轻松集群模式启动
　　3.可以无宕机重暂应用程序，保持不断连接的情况下轻松重载代码
　　4.完善的日志
　　5.自动停止不稳定的进程
6.保活应用程序

npm install pm2 -g
pm2 -v

二、操作
  举例有个express的web项目：pm2sample，端口是11111
  
  启动
  pm2 start app.js
　
  关闭
  pm2 stop 0 （为什么stop后是0？ 从上图可以看出进程ID为0，所以通过进程ID可以关闭，然后这种方式不易记，下面我看看其它方式启动和关闭）
  
  其它方式启动/关闭
  启动项目，并命名一个应用程序名
  pm2 start app.js --name test
  启动后你可以看到App name 
  
  根据App name关闭项目
  pm2 stop test
  从PM2中删除
  pm2 delete test /  也可以pm2 delete 进程ID
  
  重载和重启
  当应用程序代码有更新，可以用重载来加载新代码，也可以用重启来完成
  pm2 reload test
  pm2 restart test
  reload可以做到0秒宕机加载新的代码，restart则是重新启动，生产环境中多用reload来完成代码更新！
  
  查看详情
  pm2 show test
  
  三、多项目操作
  启动其它项目也如上面命令，我新启一个项目：pm2sample2（端口为11112）
  pm2 start app.js --name test2
  想要对这2个项目进行批量操作（多个也一样），如下(重加载全部/停止全部/重启全部/删除全部)
  pm2 reload all
  pm2 stop all
  pm2 restart all
  pm2 delete all
  
  四、集群
  启动项目列表中可以看出mode是“fork”字段值
  开发环境中多以fork的方式启动，生产环境中多用cluster方式启动
  启动方式：pm2 start app.js -i 2 --name test
  这表示启动2个并命名为test，在后台以cluster方式运行，mode为“cluster”方式，其它操作就可以通过上面用过的方式去启动、关闭、重载、重启、删除
  
  五、其它操作
   watching
   启动项目列表中有 “watching”一项，这个项默认是disabled，可以通过如下命令开启
   pm2 start app.js --name test --watch
   上面的命令中启去吧了test项目并开启了watching，这个用处主要更新代码后，不用重载或重启项目即可以立即让更新的代码起作用
　　建议：这个适合在开发时用，可以省不少时间，生产环境下最好不要用
   list
   pm2 list
　　可以列出pm2中所有项目
 
　 monit   // 用monit可以打开实时监视器去查看资源占用情况
   pm2 monit
   
   logs
    pm2 logs






  

