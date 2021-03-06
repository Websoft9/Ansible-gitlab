# 初始化安装

在云服务器上部署 GitLab 预装包之后，请参考下面的步骤快速入门。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:80** 端口是否开启
3. 若想用域名访问 GitLab，请先到 **域名控制台** 完成一个域名解析

## GitLab 安装向导

1. 使用本地电脑的 Chrome 或 Firefox 浏览器访问网址：*http://域名* 或 *http://Internet IP*, 就进入了GitLab引导页面。根据系统提示，开始重置管理员密码。
   ![GitLab初始化页面](https://libs.websoft9.com/Websoft9/DocsPicture/zh/gitlab/gitlab-createpw-websoft9.png)

2. 登陆系统（用户名是`root`，密码是上一步自行设置的） 
   ![GitLab 登录](https://libs.websoft9.com/Websoft9/DocsPicture/zh/gitlab/gitlab-login-websoft9.png)

3. 进入 GitLab 控制台，开始使用系统 
   ![GitLab 后台](https://libs.websoft9.com/Websoft9/DocsPicture/zh/gitlab/gitlab-backend-websoft9.png)

4. 进入管理设置面板（Admin Area）
   ![GitLab 管理设置面板](https://libs.websoft9.com/Websoft9/DocsPicture/en/gitlab/gitlab-adminpanel-websoft9.png)

5. 通过：【User Settings】>【Preferences】设置语言，目前已经支持中文
   ![GitLab 设置语言](https://libs.websoft9.com/Websoft9/DocsPicture/en/gitlab/gitlab-setlanguage-websoft9.png)

6. 通过：【User Settings】>【SSH key】设置秘钥
   ![GitLab SSH key](https://libs.websoft9.com/Websoft9/DocsPicture/en/gitlab/gitlab-sshkey-websoft9.png)

7. 如果你部署的是 GitLab-EE（企业版），请打开：【管理中心】>【许可证】，然后**试用**或**启用**企业版
   ![Gitlab 导入授权](https://libs.websoft9.com/Websoft9/DocsPicture/zh/gitlab/gitlabee-license-websoft9.png)

> 需要了解更多 GitLab 的使用和配置，请参考官方文档：[GitLab Documentation](https://docs.gitlab.com/omnibus/README.html)

## 常见问题

#### 浏览器打开IP地址，无法访问 GitLab（白屏没有结果）？

您的服务器对应的安全组80端口没有开启（入规则），导致浏览器无法访问到服务器的任何内容

#### GitLab能打开，但总是出现502错误？

GitLab 所需内存最低为4G，若服务器配置太低会出现502错误

#### GitLab 新装或重启后，需要等待1分钟才能使用？

对于单核CPU的服务器，Unicorn and Sidekiq 服务启动最少需要一分钟

#### 本部署包采用的哪个数据库来存储 GitLab 数据？

是PostgreSQL

#### 没有购买 License 是否可以使用 GitLab 企业版？

如果安装了 GitLab 企业版，在没有导入 License 的情况下使用的是 社区版的所有功能。[GitLab-EE vs GitLab-CE](https://about.gitlab.com/install/ce-or-ee/)

