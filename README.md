# 李紫凝 AI 聊天

## 部署到 Vercel（免费，国内可访问）

### 方法 1：用 Vercel CLI（最快）

```powershell
# 1. 安装 Vercel CLI
npm install -g vercel

# 2. 在项目目录执行
cd C:\Users\Lizining\lizining-chat
vercel

# 3. 第一次会提示登录，用 GitHub 账号登录
# 4. 一路回车用默认配置
# 5. 部署完成后会给你一个链接，比如 https://lizining-chat.vercel.app
```

### 设置 API Key

部署完后，在 Vercel 控制台：
Settings → Environment Variables → 添加：
- Key: `DEEPSEEK_API_KEY`
- Value: `sk-你的deepseek key`

添加后重新部署一次：`vercel --prod`

### 方法 2：通过 GitHub

1. 把代码推到一个 GitHub 仓库
2. 打开 vercel.com，点 "Import Project"
3. 选择你的仓库，Vercel 会自动识别 Python 项目
4. 设置环境变量 `DEEPSEEK_API_KEY`
5. 点 Deploy

---

## 本地运行

```powershell
cd C:\Users\Lizining\lizining-chat
$env:DEEPSEEK_API_KEY = "sk-你的key"
python app.py
# 打开 http://localhost:7860
```
