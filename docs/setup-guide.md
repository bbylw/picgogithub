# PicGo-GitHub 图床搭建详细指南

## 目录

- [PicGo-GitHub 图床搭建详细指南](#picgo-github-图床搭建详细指南)
  - [目录](#目录)
  - [准备工作](#准备工作)
  - [步骤一：创建 GitHub 仓库](#步骤一创建-github-仓库)
  - [步骤二：生成 GitHub Token](#步骤二生成-github-token)
  - [步骤三：配置 PicGo](#步骤三配置-picgo)
  - [步骤四：上传图片](#步骤四上传图片)
  - [步骤五：使用 Jsdelivr 加速](#步骤五使用-jsdelivr-加速)

## 准备工作

在开始之前，请确保你已经：

1. 注册了 GitHub 账户
2. 下载并安装了 [PicGo](https://github.com/Molunerfinn/PicGo/releases) 客户端

## 步骤一：创建 GitHub 仓库

1. 登录你的 GitHub 账户
2. 点击右上角的"+"按钮，选择"New repository"
3. 填写仓库名称（例如：my-image-bed）
4. 选择"Public"（必须是公开仓库）
5. 创建仓库后，确保创建 `master` 分支
6. 点击"Create repository"按钮完成创建

> **重要提示**：仓库创建后需要进行以下操作：
>
> 1. 进入仓库页面
> 2. 点击 "main" 分支选择器
> 3. 在新分支输入框中输入 `master`
> 4. 选择 "Create branch: master from 'main'"

## 步骤二：生成 GitHub Token

1. 点击右上角的头像，选择"Settings"
2. 在左侧菜单中，选择"Developer settings"
3. 点击"Personal access tokens"，然后选择"Tokens (classic)"
4. 点击"Generate new token"按钮
5. 填写名称，勾选"repo"权限（需要完整的仓库访问权限）
6. 生成后立即复制 Token（Token 只显示一次！）

## 步骤三：配置 PicGo

1. 打开 PicGo 软件
2. 点击左侧的"图床设置"
3. 选择"GitHub图床"
4. 填写配置信息：
   - 仓库名：`你的用户名/my-image-bed`
   - 分支名：`master`（必须使用 master 分支）
   - Token：粘贴之前生成的 Token
   - 存储路径：可以设置为 `img/`
   - 自定义域名：可选，使用 JSDelivr 加速必须填写：`https://cdn.jsdelivr.net/gh/用户名/仓库名@master`

## 步骤四：上传图片

1. 在 PicGo 中点击"上传区"
2. 选择要上传的图片或直接拖拽图片到上传区
3. 等待上传完成，PicGo 会自动复制图片链接到剪贴板

## 步骤五：使用 Jsdelivr 加速

要使用 JSDelivr CDN 加速，只需将图片链接格式修改为：

```plaintext
https://cdn.jsdelivr.net/gh/用户名/仓库名@master/图片路径
```

例如：

```plaintext
https://cdn.jsdelivr.net/gh/your-username/my-image-bed@master/img/example.png
```
