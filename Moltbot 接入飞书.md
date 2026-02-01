## ▶️配置之前的准备工作
1. 准备飞书开发者账号，开启一个企业应用
[飞书开发者平台地址](https://open.feishu.cn/app?lang=zh-CN)
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/bd34a258-1aaf-4cf2-a4d7-65b2ddf036c7.png "image.png")
添加一下机器人
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/1c8aa841-4b20-465d-9dec-3773b5584346.png "image.png")
需要在飞书应用内开启权限
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/0afb68e2-77ee-4f80-b840-f6321c00574e.png "image.png")
将一下权限导入并开通
```json
{
  "scopes": {
    "tenant": [
      "im:chat:readonly",
      "im:message.group_at_msg:readonly",
      "im:message.p2p_msg:readonly",
      "im:message:readonly",
      "im:message:send_as_bot",
      "im:resource"
    ],
    "user": [
      "contact:user.base:readonly",
      "im:message",
      "im:message.pins:read",
      "im:message.pins:write_only",
      "im:message.reactions:read",
      "im:message.reactions:write_only",
      "im:message.urgent.status:write",
      "im:message:readonly",
      "im:message:recall",
      "im:message:update"
    ]
  }
}
```
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/ab2e2368-0287-4d0e-94c1-20434246a400.png "image.png")
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/12b9f157-ab4d-46f8-8392-63ec14593928.png "image.png")
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/167e48b1-7d79-492f-bd9e-8568930328a3.png "image.png")
> 这样权限就是配置好了，当然如果需要更多配置可以自己去研究。目前给出的是最小可用基本配置
## 🚀现在去moltbot中配置飞书的内容
1. 添加飞书的组件
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/485d3bf3-9f99-4943-8855-09c41a2f1653.png "image.png")
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/b0a109e1-18e3-40a8-b4c9-7fe2d027ae3b.png "image.png")
```bash
## 这几个命令一个一个讲
## 首先进入到工作目录
cd /home/node/clawd
## 下载飞书的插件（必须是0.1.2这个版本，更新的就不兼容了）
curl -O https://registry.npmjs.org/@m1heng-clawd/feishu/-/feishu-0.1.2.tgz
## 安装插件 moltbot 命令需要替换为 node /app/dist/index.js
node /app/dist/index.js plugins install ./feishu-0.1.2.tgz
```
> 你的结果和我的应该不一样，应该是提示安装成功，我的因为已经安装过，所以提示插件存在了
如果上面的链接下载不了包，可以使用这个

2. moltbot添加飞书配置
当上面的插件安装好了，在`channels`里面就可以看到飞书的插件了。
**⚠️如果飞书这个不存在的话，多刷新几次页面，就会出来了。如果实在没出来，请重启这个应用！！！
⚠️如果飞书这个不存在的话，多刷新几次页面，就会出来了。如果实在没出来，请重启这个应用！！！
⚠️如果飞书这个不存在的话，多刷新几次页面，就会出来了。如果实在没出来，请重启这个应用！！！**
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/67caab53-3b79-4e88-9e03-ab7a3c9d112c.png "image.png")
⚠️如果你不懂配置的话，以下配置建议完全一致！！！
⚠️如果你不懂配置的话，以下配置建议完全一致！！！
⚠️如果你不懂配置的话，以下配置建议完全一致！！！
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/0027fdcc-872f-4eef-8ede-b71c0b8b4954.png "image.png")
飞书的`App id` 和`App Secret` 从飞书开发者获取到
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/d0c1edf4-e2ca-4cc7-936d-81ec56b8bc5c.png "image.png")
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/6be17e26-ce18-44f4-a7fa-1ba14d010b36.png "image.png")
## 重新回飞书配置
配置微服长连接
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/ea9e1d9b-7991-45f3-b481-caea1ef2d063.png "image.png")
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/3fdd7d49-d2b3-46b9-9d97-09ad847c052d.png "image.png")
⚠️如果出现链接不可用，请再三确认moltbot中的配置是否正确
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/d6b443e2-b04f-490a-bccd-baade0352b1a.png "image.png")
添加如下事件：


| 事件编码                          | 说明             |
|-----------------------------------|------------------|
| `im.message.receive_v1`          | 接收消息（必需） |
| `im.message.message_read_v1`     | 消息已读回执     |
| `im.chat.member.bot.added_v1`    | 机器人进群       |
| `im.chat.member.bot.deleted_v1`  | 机器人被移出群   |

配置好了之后，一定要创建发布一个应用版本
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/0b2362bd-68e9-494d-86c0-a1dee6caf62d.png "image.png")
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/9c7ec829-0570-4fe3-bcb7-933f4f26330e.png "image.png")

## 测试
如果上面的配置都好了之后，可以去飞书里面测试了。
群聊添加机器人
![image.png](https://lzc-playground-1301583638.cos.ap-chengdu.myqcloud.com/guidelines/439/ffd05995-589e-4e42-ad65-368a7dce015c.png "image.png")
