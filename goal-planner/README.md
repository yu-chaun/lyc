# 目標理財規劃師

利用 PV（現值）、FV（終值）、PMT（每期定額）的理財目標試算網站。純前端、單一 HTML 檔，不需要建置或後端。

## 功能
- 依目標金額、年限、現有本金與報酬率，反推每月所需存款（PMT）
- 計算目前計畫的預估終值（FV）、一次投入所需現值（PV）、達標時間與所需報酬率
- 通膨調整、資產成長曲線圖、不同報酬率情境表與調整建議

## 專案結構
```
goal-planner/
├── public/
│   └── index.html   # 整個網站
├── README.md
└── .gitignore
```

## 本機預覽
直接用瀏覽器開啟 `public/index.html` 即可。

## 上傳到 GitHub
```bash
cd goal-planner
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<你的帳號>/<倉庫名稱>.git
git push -u origin main
```

## 部署到 Cloudflare Pages
1. Cloudflare 後台 → Workers & Pages → Create → Pages → Connect to Git
2. 選擇這個 GitHub 倉庫
3. 建置設定：
   - Framework preset：None
   - Build command：留空
   - Build output directory：`public`
4. Save and Deploy，完成後會得到 `*.pages.dev` 網址

之後每次 push 到 `main`，Cloudflare 都會自動重新部署。

## 注意
本工具僅為教育用途的試算（每月複利、期末存入），不構成投資建議。
