# 作品名称 
马佳源的数字名片

## 项目简介
这是一个个人数字名片页面，展示了马佳源的基本信息、兴趣爱好、技能特长等内容。

## 在线访问
[点击这里访问在线页面](https://songshishie.github.io/mjy.github.io/)


## 项目结构
my_website_tag/
├── index.html          # 主页面
├── style.css           # 样式文件
├── images/             # 图片目录
│   └── photo.jpg       # 个人照片
└── README.md           # 项目说明文档


## 本地预览
直接在浏览器中打开 `index.html` 文件即可预览。


## 部署说明

### 本地预览
直接在浏览器中打开 `index.html` 文件即可预览。

### GitHub Pages 部署
本项目已部署到 GitHub Pages：
- 网址：https://songshishie.github.io/mjy.github.io/
- GitHub 仓库：https://github.com/songshishie/mjy.github.io

### Gitee 部署
- Gitee 仓库：https://gitee.com/ma-jiayuan21/my-web-tag
- 注意：Gitee Pages 服务已暂停，仅作为代码托管使用

### 同时推送到 Gitee 和 GitHub

#### 方法一：配置多个推送地址（推荐）

1. **查看当前远程仓库配置**
   ```bash
   git remote -v
   ```

2. **为 origin 添加多个推送地址**
   ```bash
   # 先设置 origin 的拉取地址为 Gitee
   git remote set-url origin https://gitee.com/ma-jiayuan21/my-web-tag.git
   
   # 添加 Gitee 推送地址
   git remote set-url --add --push origin https://gitee.com/ma-jiayuan21/my-web-tag.git
   
   # 添加 GitHub 推送地址
   git remote set-url --add --push origin https://github.com/songshishie/mjy.github.io.git
   ```

3. **验证配置**
   ```bash
   git remote -v
   ```
   应该看到：
   - fetch 地址指向 Gitee
   - push 地址有两个：Gitee 和 GitHub

4. **使用方法**
   ```bash
   # 正常提交代码
   git add .
   git commit -m "更新内容"
   
   # 一次推送到两个平台
   git push origin main
   ```

#### 方法二：使用 Git 钩子脚本

1. **创建 post-commit 钩子**
   在 `.git/hooks/post-commit` 文件中添加：
   ```bash
   #!/bin/sh
   git push gitee main
   git push github main
   ```

2. **配置两个 remote**
   ```bash
   git remote add gitee https://gitee.com/ma-jiayuan21/my-web-tag.git
   git remote add github https://github.com/songshishie/mjy.github.io.git
   ```

3. **使用方法**
   ```bash
   git add .
   git commit -m "更新内容"
   # 自动推送到两个平台
   ```

#### 方法三：使用别名一键推送

1. **配置 Git 别名**
   ```bash
   git config --global alias.pushall '!git push gitee main && git push github main'
   ```

2. **配置两个 remote**
   ```bash
   git remote add gitee https://gitee.com/ma-jiayuan21/my-web-tag.git
   git remote add github https://github.com/songshishie/mjy.github.io.git
   ```

3. **使用方法**
   ```bash
   git add .
   git commit -m "更新内容"
   git pushall
   ```

### 注意事项

1. **权限配置**：确保你已经在两个平台都配置了 SSH 密钥或保存了账号密码
2. **分支名称**：确认两个仓库的主分支名称一致（main 或 master）
3. **首次推送**：如果是新仓库，需要先用 `git push -u origin main` 设置上游分支
4. **冲突处理**：如果某个平台推送失败，另一个平台仍会成功推送



## 联系方式

- 姓名：马佳源
- 学号：2362120121
- 专业：计算机科学与技术
- 电话：19857670795

## 页面主要内容
- 个人照片：/images/photo.jpg
- 个性签名：跳出三贷之外，不在五险之中
- 关于我：毕业于家里蹲大学、屋里系、床上专业，主攻方向是“睡眠深度学与梦境潜意识开发”。曾在 “腾讯公益：捐步数” 项目中担任核心执行者，为腾讯服务器贡献了大量无效运动数据。具备丰富的 “摸鱼管理经验” ，擅长在不被发现的前提下，把8小时工作时间拉伸成24小时的充实感。我是国家级非物质文化遗产——“嘴硬”的传承人，擅长领域包括：我没胖、我不困、这很简单。主要研究课题：“如何用脚趾抠出三室一厅”的可行性分析。
- 兴趣爱好：看小说、看直播、玩游戏
- 技能特长：饭点会饿、饿了会找吃的、吃了会睡
- 外部链接：https://gitee.com/ma-jiayuan21/my-web-tag
           https://github.com/songshishie/mjy.github.io


#AI辅助开发说明
1、使用AI辅助开发
2、使用智能体通义灵码、deepseek
3、“搭建静态页面框架”、“帮我添加功能......”、“生成README.md”
4、智能体完善框架，具体信息自行修改，然后不懂的地方问Deep Seek
5、一般是对AI生成的布局不满意，然后提出更细节的要求
6、AI会给出过时的方案，比如说静态页面部署使用gitee Page，但是这个服务已经暂停