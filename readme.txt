===============================
六班17组唐文龙DjangoBlog 博客系统作业
===============================

【项目说明】
本程序为个人软件工程课程作业，仅用于本人课程学习、实践及考核相关用途，非商业用途。
本项目基于优秀开源项目 DjangoBlog 进行学习与二次实践，感谢原作者的杰出开源贡献！
项目内容为个人学习实践产出，由于个人能力有限，难免存在疏漏或不当之处，还请老师及同学多多指正。

【项目简介】
本项目是一个基于 Python 和 Django 开发的简单个人博客系统，包含文章发布、评论、用户管理、后台管理等基础功能，用于完成软件工程课程的实践作业。

【环境依赖/运行环境】
- 操作系统：Windows 10 / Windows 11
- Python 版本：3.8 及以上 (推荐 3.10 或 3.11)
- 数据库：MySQL 5.7 或 8.0 版本
- Web 框架：Django 3.x / 4.x 版本 (具体以 requirements.txt 为准)
- 数据库驱动：mysqlclient 或 pymysql (需根据项目配置选择)
- 依赖管理工具：pip

【如何运行（Windows 环境 + MySQL 数据库）】
1. 下载项目代码到本地，并进入项目根目录（例如 D:\6班19组\src）。
2. 打开命令行（CMD 或 PowerShell），创建并激活虚拟环境（推荐）：
   python -m venv venv
   venv\Scripts\activate
3. 安装项目所需依赖库：
   pip install -r requirements.txt
   (若缺少 MySQL 驱动，请执行：pip install mysqlclient 或 pip install pymysql)
4. 在本地 MySQL 中创建数据库（例如名为 djangoblog）：
   CREATE DATABASE djangoblog CHARACTER SET utf8mb4;
5. 修改项目数据库配置（通常在 djangoblog/settings.py 中）：
   将 DATABASES 配置项修改为本地 MySQL 连接信息（NAME, USER, PASSWORD, HOST, PORT）。
6. 初始化数据库（生成表结构）：
   python manage.py migrate
7. 创建后台管理员账号（方便登录后台，按提示输入用户名和密码）：
   python manage.py createsuperuser
8. 启动本地开发服务器：
   python manage.py runserver
9. 打开浏览器访问：
   前台地址：http://127.0.0.1:8000/
   后台地址：http://127.0.0.1:8000/admin/

【目录结构说明（src 目录下的主要结构）】
- accounts/     : 用户账号管理模块（注册、登录、个人资料等）
- blog/         : 博客核心功能模块（文章、分类、标签、搜索等）
- comments/     : 评论系统模块（文章评论、回复等）
- deploy/       : 部署相关配置文件
- djangoblog/   : 项目核心配置目录（settings.py, urls.py 等）
- docs/         : 项目相关文档资料
- frontend/     : 前端静态资源文件（CSS、JS、图片等）
- locale/       : 国际化与本地化翻译文件
- oauth/        : 第三方登录认证模块
- plugins/      : 插件扩展目录（如文章推荐、侧边栏等）
- servermanager/: 服务器管理后台相关代码
- templates/    : HTML 模板文件
- manage.py     : Django 项目管理工具脚本
- requirements.txt : 项目所需依赖包清单

【致谢】
再次感谢 DjangoBlog 开源项目及原作者的无私分享，为本人的课程学习提供了宝贵的实践素材