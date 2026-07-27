# 换电脑恢复指南

> 把 `我的工作台` 文件夹拷到新电脑后，看这个文件。

---

## 首次恢复（在新电脑上）

### 1. 装 Git for Windows
https://git-scm.com/download/win

安装时一路点 Next 就行。

### 2. 拉取工作台

打开终端（在要放工作台的文件夹里输 `powershell`），打：

```powershell
git clone https://github.com/2274955796/houshen.git
```

整个工作台就回来了。

### 3. 配置 Git 身份

```powershell
git config --global user.name "caleb_xiaohou"
git config --global user.email "2274955796@qq.com"
```

### 4. 验证

打开 Claude Code，说一句「状态」确认一切正常。

---

## GitHub Token（push 时需要）

如果 push 时让你登录：去 https://github.com/settings/tokens 生成新 Token，勾选 `repo` 权限，过期选 No expiration。然后在终端里重新设置远程地址：

```powershell
git remote set-url origin https://你的token@github.com/2274955796/houshen.git
```
