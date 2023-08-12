# Latex

## Mac

### 1.下载

**Latex运行必备环境MacTex：**[http://www.tug.org/mactex/](http://www.tug.org/mactex/)

**VS code编辑器：**[https://code.visualstudio.com/](https://code.visualstudio.com/)

### 2. 安装 Latex Workshop插件

### 3. 修改user setting

**打开setting，找到USER->Extensions->JSON->settings.json，配置以下内容**

```
 {
 
     "latex-workshop.latex.recipes": [{
 
     "name": "xelatex",
 
     "tools": [
 
         "xelatex"
 
     ]
 
   }, {
 
     "name": "latexmk",
 
     "tools": [
 
         "latexmk"
 
     ]
 
   },
 
   {
 
     "name": "pdflatex -> bibtex -> pdflatex*2",
 
     "tools": [
 
         "pdflatex",
 
         "bibtex",
 
         "pdflatex",
 
         "pdflatex"
 
     ]
 
   }
 
   ],
 
   "latex-workshop.latex.tools": [{
 
   "name": "latexmk",
 
   "command": "latexmk",
 
   "args": [
 
     "-synctex=1",
 
     "-interaction=nonstopmode",
 
     "-file-line-error",
 
     "-pdf",
 
     "%DOC%"
 
   ]
 
   }, {
 
   "name": "xelatex",
 
   "command": "xelatex",
 
   "args": [
 
     "-synctex=1",
 
     "-interaction=nonstopmode",
 
     "-file-line-error",
 
     "%DOC%"
 
   ]
 
   }, {
 
   "name": "pdflatex",
 
   "command": "pdflatex",
 
   "args": [
 
     "-synctex=1",
 
     "-interaction=nonstopmode",
 
     "-file-line-error",
 
     "%DOC%"
 
   ]
 
   }, {
 
   "name": "bibtex",
 
   "command": "bibtex",
 
   "args": [
 
     "%DOCFILE%"
 
   ]
 
   }],
 
   "latex-workshop.view.pdf.viewer": "tab",
 
   "latex-workshop.latex.clean.fileTypes": [
 
   "*.aux",
 
   "*.bbl",
 
   "*.blg",
 
   "*.idx",
 
   "*.ind",
 
   "*.lof",
 
   "*.lot",
 
   "*.out",
 
   "*.toc",
 
   "*.acn",
 
   "*.acr",
 
   "*.alg",
 
   "*.glg",
 
   "*.glo",
 
   "*.gls",
 
   "*.ist",
 
   "*.fls",
 
   "*.log",
 
   "*.fdb_latexmk"
 
   ],
 
 }
```

### 4. 重启VSCode

### 5. 测试

**写入**

```
 \documentclass{article}
 
 \begin{document}
 
 hello,world
 
 \end{document}
```

**点击Recipe: xelatex即可编译，预览**


# Go

Mac

[原文](https://zhuanlan.zhihu.com/p/143254415)

[vscode](https://code.visualstudio.com/)

[golang](https://golang.org/dl/)

#### 设置gopath

```
 go env -w GOPATH=/Users/daijing/go
```

#### 设置goMod状态

```
 go env -w GO111MODULE=on
 go env -w GOPROXY=https://goproxy.cn,direct
```

#### 配置vscode

**下载Go插件**

![img](https://pic3.zhimg.com/80/v2-d52a52ccb37accb641ca31fbb74a406e_720w.jpg)

**vscode自动补全**

**shift + command + p**

```
 Go: Install/Update tools
```

**进入setting.json**

```
 "go.inferGopath": true,
 "go.useCodeSnippetsOnFunctionSuggest": true,
```
