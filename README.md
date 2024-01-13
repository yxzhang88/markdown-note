
# 安装和使用

在 Vim 中实时预览 Markdown 文件时，可以使用 `vim-instant-markdown` 插件。以下是总结的步骤：

1. **安装 Node.js 和 npm：**
确保你的系统上安装了 Node.js 和 npm。你可以从官方网站 [Node.js 官网](https://nodejs.org/) 下载安装。
2. **安装 nvm（可选）：**
你可以选择使用 `nvm`（Node.js 的版本管理器）安装 Node.js，这可以避免权限问题。在终端中运行以下命令安装 `nvm`：
    
    ```bash
    curl -o- <https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh> | bash
    
    ```
    然后重新启动终端或运行 `source ~/.zshrc`（或 `source ~/.bashrc`）。
    
3. **使用 nvm 安装 Node.js：**
在终端中运行以下命令安装 Node.js：
    
    ```bash
    nvm install node
    
    ```
    
4. **安装 instant-markdown-d：**
在终端中运行以下命令安装 `instant-markdown-d`：
    
    ```bash
    npm install -g instant-markdown-d
    
    ```
    
5. **安装 vim-instant-markdown 插件：**
在 Vim 的配置文件中（通常是 `~/.vimrc`）添加以下内容：
    
    ```
    call plug#begin('~/.vim/plugged')
    " Specify your plugins here
    Plug 'suan/vim-instant-markdown'
    call plug#end()
    
    ```
    保存并关闭文件，然后在终端中运行以下命令安装插件：
    
    ```
    vim +PlugInstall +qall
    
    ```
    
6. **运行 Vim：**
打开一个 Markdown 文件，进入普通模式，然后运行以下命令：
    
    ```
    :InstantMarkdownPreview
    
    ```
    这将在你的默认浏览器中打开实时预览。

# 和github连接
### 1. 创建 GitHub 仓库：

1. 在 GitHub 上登录你的帐户。
2. 在页面右上角点击加号 (+)，然后选择 "New repository"。
3. 输入仓库名称、描述等信息，选择是否添加 **`.gitignore`** 文件和许可证，然后点击 "Create repository"。

### 2. 克隆仓库到本地：

在你的本地计算机上打开终端，运行以下命令：

```bash
bashCopy code
git clone <repository_url>
cd <repository_name>
```

### 3. 创建并编辑 Markdown 文件：

使用你喜欢的文本编辑器创建一个 Markdown 文件，例如 **`sample.md`**，并在其中添加一些内容。

### 4. 添加、提交和推送更改：

在终端中运行以下命令：

```bash

git add sample.md
git commit -m "Add sample Markdown file"
git push origin main
```

#### Personal Access Token创建
- GitHub 不再支持使用密码进行身份验证。相反，建议使用个人访问令牌 (Personal Access Token, PAT) 进行身份验证。下面是如何使用个人访问令牌进行身份验证的步骤：
    1. 在 GitHub 上生成个人访问令牌：
        - 进入 [GitHub Settings](https://github.com/settings/profile).
        - 在左侧导航栏中选择 "Developer settings" > "Personal access tokens".
        - 点击 "Generate token" 按钮，设置访问范围，并生成令牌。
    2. 复制生成的个人访问令牌。
    3. 在命令行中使用个人访问令牌进行身份验证：
        
        ```bash
        git push origin main
        
        ```
    在提示输入用户名和密码时，使用你的 GitHub 用户名作为用户名，并将个人访问令牌粘贴为密码。确保使用 HTTPS URL 进行推送。
    

### 5. 查看 Markdown 文件：

在 GitHub 仓库页面上，你应该能够在文件列表中看到 **`sample.md`** 文件。点击它以查看内容。


# Markdown cheat sheet
https://www.markdownguide.org/cheat-sheet/

https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

https://support.squarespace.com/hc/en-us/articles/206543587-Markdown-cheat-sheet

https://markdown-it.github.io/ 
