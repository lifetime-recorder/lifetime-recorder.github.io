### Introduction
)The readme file has chinese version behind.（中文版说明在最下面。）

### What is lifetime-recorder?
1. We try our best to trace the changes about person year by year,until we can not contact with them.We call them as VIP.
2. Every year,we do a interview and ask some meaningful and interesting questions for every VIP.
3. We record the interview as a vedio and put it at this website with if our VIP permit about this.
4. Every one can contact us to became a new VIP,or add some interesting questions your want to ask VIP.
5. Just send emails to oraant777@gmail.com if you want to contact us.

### Add User To Home Page:
1. add file at `_data/vip.yml/(new_user)`
2. add global image at `qiniu/lifetime/vips/(new_user)/global-head.jpg`
3. add record file at `_data/vips/(new_user)`

### Add Record To User:
1. add record at `_data/vips/(user)`
2. add record image at `qiniu/lifetime/vips/(user)/(year)-head.jpg`
3. add post at `_post/(user)/(year)-(month)-(day)-(new_user)-(year).md`
4. add post image at `qiniu/lifetime/vips/(user)/(year)-(desc).jpg`
5. add vedio at `bilibili.com`

### To do things:
1. make a logo for the website,and try to find some better images.
2. edit one post use markdown,and upload ralation images and vedios to some where.maybe bilibili is a good choice.
4. add duoshuo comment to the template.add google analyse.
6. prepare new questions,and watch match more interviews online,and learn how to do it.
3. test on different screen,and modify them.

### 介绍
1. 网站层：最外层的index.html/vips.html/about.html/encourage.html，是网站的四个大页面。
  - vips.html展现所有贵宾的一个简介及其主页的链接，这需要从_data/vip.yml中读取数据
2. 主页层：vips/xxx-name.html，是每个vip的主页，展示了这个vip完整的一生中，所有的采访记录
  - vips/xxx-name.html不过是_layout/life.html类的一个实例，需要根据实例的vip_code中，从_data/vip.yml中读取贵宾信息（如名称和签名），并从_data/vips/xxx-name.yml中，读取每年的记录。
3. 文章层：_posts/xxx-name/yyyy-mm-dd-xxx-name-yyyy.md，是每个vip具体某一年的详细记录描述，包括了其采访内容简介及视频链接等
  - /xxx-name/文件夹是为了方便分组管理，无实际作用
  - yyyy-mm-dd-xxx-name-yyyy.md是文章时间-编号-姓名-记录编号，记录编号指的2016年或2017年这种的，一开始的设计中考虑到了可能会有2016a，2016b这种的，将来可以考虑取消掉
  - xxxxx.md是_layouts/post.html类的一个实例，在表头注明自己的贵宾编号（vip_code）和记录编号（record_year），post.html从vips/xxx-name.yml中提取本年的编号、签名、头像等。

### 需要问的问题
