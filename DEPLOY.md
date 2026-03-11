# 部署到 Gitee Pages 的详细步骤

## 第一步：在 Gitee 创建仓库

1. 访问 https://gitee.com/
2. 登录你的 Gitee 账号
3. 点击右上角的 "+" 号，选择"新建仓库"
4. 填写仓库信息：
   - 仓库名称：my_website_tag
   - 其他选项保持默认即可
5. 点击"立即创建"

## 第二步：关联远程仓库并推送代码

### 方法一：使用 HTTPS（推荐）

在项目根目录执行以下命令：

```bash
# 将 <你的 Gitee 用户名> 替换为你的实际用户名
git remote add origin https://gitee.com/<你的 Gitee 用户名>/my_website_tag.git

# 推送代码到 Gitee
git push -u origin master
```

### 方法二：使用 SSH

如果你已经配置了 SSH 密钥：

```bash
# 将 <你的 Gitee 用户名> 替换为你的实际用户名
git remote add origin git@gitee.com:<你的 Gitee 用户名>/my_website_tag.git

# 推送代码到 Gitee
git push -u origin master
```

## 第三步：启用 Gitee Pages 服务

1. 进入你刚创建的仓库页面
2. 点击顶部菜单的"服务"
3. 在左侧菜单找到"Gitee Pages"
4. 配置 Pages 服务：
   - 源分支：选择 `master`
   - 根目录：保持 `/`
5. 点击"保存"按钮

## 第四步：访问你的数字名片

保存成功后，你会看到一个访问地址，格式为：
```
https://<你的 Gitee 用户名>.gitee.io/my_website_tag/
```

点击该链接即可访问你的数字名片页面！

## 第五步：完善个人信息

### 1. 添加个人照片

- 准备一张个人照片或卡通形象
- 将照片命名为 `photo.jpg`
- 放入项目的 `images/` 目录
- 提交并推送：

```bash
git add images/photo.jpg
git commit -m "添加个人照片"
git push
```

### 2. 填写自我介绍

编辑 `index.html` 文件，找到注释 `<!-- 请在此处填写您的自我介绍，不少于 100 字 -->`，在其下方添加你的自我介绍内容。

例如：
```html
<p class="about-text">
    你好！我是马佳源，一名计算机科学与技术专业的大学生。我热爱编程，喜欢探索新技术，
    对前端开发有着浓厚的兴趣。平时我喜欢看小说、看直播和玩游戏，这些爱好让我的生活更加丰富多彩。
    我相信通过不断学习和实践，我能够成为一名优秀的程序员。期待与更多人交流学习！
</p>
```

然后提交并推送：
```bash
git add index.html
git commit -m "更新自我介绍"
git push
```

### 3. 添加外部链接

编辑 `index.html` 文件，找到 `.external-link` 部分，修改 `href` 属性为你的链接地址。

例如：
```html
<a href="https://github.com/yourusername" class="external-link" target="_blank">
    我的 GitHub
</a>
```

然后提交并推送：
```bash
git add index.html
git commit -m "更新外部链接"
git push
```

## 注意事项

1. **图片命名**：确保你的照片命名为 `photo.jpg`，或者修改 `index.html` 中的图片路径
2. **更新页面**：每次推送代码后，Gitee Pages 会自动更新，但可能需要几分钟时间生效
3. **浏览器缓存**：如果页面没有更新，尝试清除浏览器缓存或强制刷新（Ctrl+F5）

## 常见问题

### Q: 推送代码时提示权限错误？
A: 检查远程仓库地址是否正确，确认你有该仓库的写入权限。

### Q: Pages 服务无法启用？
A: 确保仓库不是私有的，且已经提交了 index.html 文件。

### Q: 页面样式不正常？
A: 检查 CSS 文件路径是否正确，清除浏览器缓存后重试。

---

祝你部署顺利！如有问题，欢迎联系。
