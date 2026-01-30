# Clawdbot 接入飞书！手把手教学！

### 家人们！2026 爆火的开源 AI 智能体 Clawdbot（现已更名 Moltbot）重磅更新！微服务部署轻松搞定，现在还能无缝接入飞书，办公提效直接拉满！

如果您也有将Clawdbot 接入飞书的需求，那么以下教程将帮助您顺利接入！
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/0428ea15-51cb-41f9-9f4b-c60b0d99612a.png "image.png")

首先，请确保您已经配置好Moltbot且可以正常对话，如果您没有配置好，请参考https://lazycat.cloud/playground/guideline/1488

确保正常能正常对话之后，登录飞书开放平台 https://open.feishu.cn ，点击「开发者后台 -> 创建企业自建应用」，如下图
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/b91776a2-da24-4334-b393-02a20bc4e584.png "image.png")

然后点击创建应用，如下

![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/c9f07237-17b8-4dcd-9765-54670b5b1490.png "image.png")

创建完成后，首先到凭据管理中获取 App ID 和 App Secret，注意保存，后续配置需要使用。

![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/e87ca317-6cf7-4432-9605-88b1f692ce39.png "image.png")

然后添加机器人，如下操作

![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/9ea8485e-6dc2-4c65-a15c-4da6ce58d424.png "image.png")

配置一个名字，点击保存即可。

**接下来我们来打通两者的链接**

如果您动手能力强，请根据https://github.com/m1heng/clawdbot-feishu?tab=readme-ov-file#english 此文章来进行配置

那么有没有简单一点的方式来配置呢？


既然我们已经可以跟Clawdbot来对话了，自然我们也可以发布指令，让他来帮我们进行全自动操作。因为对接只需要我们提供我们刚刚获取的飞书App ID和App Secret即可

那我们来到chat，对他发布指令：https://github.com/m1heng/clawdbot-feishu?tab=readme-ov-file#english 请根据这一篇文章，帮我把你对接到飞书，APP ID是XXXXXXXX，App Secre是XXXXXXXXX。


![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/928233a9-eb5e-4870-8994-7483a88ec4d5.png "image.png")

然后我们只需静静等待他默默修改自己的配置（**途中可能会和服务器断开连接数次，我们在微服中重启Clawdbot，然后打开应用，发布命令让他继续执行即可**）


![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/06d3b235-b712-4290-bbe6-de02b4f6313c.png "image.png")
等AI执行完他所需要的操作之后，他会告知你让你来进行最后的飞书操作（配置自己需要用到的机器人权限），我们根据他总结的步骤一步步操作即可，不明白的可以让AI给出详细操作步骤。

![拼接图片_1769764358967 (1).jpg](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/235a2940-a2da-4348-8362-feb1df739852.jpg "拼接图片_1769764358967 (1).jpg")

以上步骤全部完成后，即可与机器人对话。但在此之前需要先创建一个版本

![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/703c5879-6c62-450b-bbd9-3d34675b6dfe.png "image.png")

发布完成后，回到飞书客户端，可以看到应用已上线，点击打开应用
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/1bbcc8cf-4a74-4d93-851c-5fdd626594f6.png "image.png")

飞书能登陆的地方都随意问答~

![拼接图片_1769764770101.jpg](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/1080/d2a2dce8-2824-44d8-ba2d-d1a86275438a.jpg "拼接图片_1769764770101.jpg")