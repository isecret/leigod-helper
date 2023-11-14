## ⚡️雷神加速器暂停助手

⚡️基于雷神加速器 Web 接口实现自动登录和暂停计时

## 使用方法

部署本地或服务器中，需先安装依赖；

```bash
# Ubuntu/Debain
$ sudo apt-get install -y jq

# CentOS
$ sudo yum install -y jq

# MacOS
$ sudo brew install -y jq
```

克隆仓库或下载代码包并解压；

```bash
git clone --depth=1 https://github.com/isecret/leigod-helper.git
# 因为国内网络克隆速度不是很理想的，选择下面的
git clone --depth=1 https://ghproxy.com/github.com/isecret/leigod-helper.git
```

修改配置，编辑 `leigod-helper.sh` 修改用户名和密码；

```bash
# 手机号
USERNAME="18866668888"
# 密码
PASSWORD="password"
```

保存编辑，添加脚本可执行权限并尝试运行；

```bash
$ sudo chmod +x leigod-helper.sh && ./leigod-helper.sh
暂停结果: ...
```

添加定时任务定时自动执行；

```bash
# 每天凌晨 2:00 暂停计时
0 2 * * * bash /path/to/leigod-helper.sh >> /path/to/leigod-helper.log 2>&1
```

## Todo
- 任务通知