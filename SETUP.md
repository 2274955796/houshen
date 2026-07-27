# 换电脑恢复指南

> 把 `我的工作台` 文件夹拷到新电脑后，看这个文件。

---

## 一步恢复

在新电脑的终端里跑：

```powershell
# 1. 把 skills 目录下的技能都挂到 Claude Code
Copy-Item -Recurse -Force "$PWD\skills\*" "$env:USERPROFILE\.claude\skills\"

# 2. 验证
Write-Host "Skills installed:"; Get-ChildItem "$env:USERPROFILE\.claude\skills" | Select-Object Name
```

## 还需要装的东西

| 工具 | 干嘛的 | 下载 |
|------|--------|------|
| Claude Code | 本体 | 官网安装 |
| Git for Windows | 从 GitHub 下载 skill 更新 | https://git-scm.com |

## 首次使用

拷完后在新电脑上打开 Claude Code，说一句「状态」确认一切正常就行。
