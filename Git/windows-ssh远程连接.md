2025年2月12日

本意想远程访问。想通过在Windows上部署code-cserver，但是没看懂。

- https://lsq.world/index.php/2022/10/29/codeserver%E6%90%AD%E5%BB%BA/
- https://blog.bloade.com/2022/12/03/%E5%B0%86%E6%9C%AC%E5%9C%B0%E9%83%A8%E7%BD%B2visual-studio-code-server%E4%BD%9C%E4%B8%BA%E6%9C%8D%E5%8A%A1/

继续在Windows上部署ssh服务，通过远程访问。

原先是公网无法访问，经过请教后使用花生壳进行公网访问。

以下是参考资料。



使用该教程打开ssh服务：https://www.cpolar.com/blog/install-ssh-on-windows-and-connect-to-the-ssh-service-remotely-without-a-public-ip-address

通过Windows powershell打开👇

```bash
Start-Service sshd
```

查看ssh服务当前状态

```bash
Get-Service sshd
```

![image-20250212182107289](https://typora-urname.oss-cn-beijing.aliyuncs.com/git/20250212182107344.png)

以及我使用的端口是22。

![image-20250212182335911](https://typora-urname.oss-cn-beijing.aliyuncs.com/git/20250212182335938.png)

另外，获取本地用户名称时需要从cmd中查看。

![image-20250212182244381](https://typora-urname.oss-cn-beijing.aliyuncs.com/git/20250212182244412.png)

接着再在visual studio中输入ssh Name@ip -A，就可以了。

---



我的Windows可选功能用不了了。所以使用原先的参考也不管用。

https://blog.csdn.net/weixin_72910567/article/details/132414264

![image-20250212182424564](https://typora-urname.oss-cn-beijing.aliyuncs.com/git/20250212182424630.png)



---



剩余的参考链接

- Windows开启ssh（普通，失败）：https://cloud.tencent.com/developer/article/1420930
- Windows开启ssh（失败）：https://zhuanlan.zhihu.com/p/391373172

