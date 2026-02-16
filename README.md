# 躍馬迎春：紅包大作戰 🐴🧧

馬年新春 HTML5 Canvas 遊戲

## 遊戲玩法

- 按空白鍵或點擊螢幕跳躍
- 避開鞭炮障礙物
- 收集紅包得分

## 部署到 GitHub Pages

### 步驟 1: 推送代碼到 GitHub

```bash
git init
git add .
git commit -m "Initial commit: Horse Year Game"
git branch -M main
git remote add origin https://github.com/你的帳號/horse-year-games.git
git push -u origin main
```

### 步驟 2: 啟用 GitHub Pages

1. 前往 Repository **Settings** > **Pages**
2. **Source** 選擇 `main` 分支
3. 點擊 **Save**
4. 等待部署完成（約 1-2 分鐘）
5. 訪問 `https://你的帳號.github.io/horse-year-games/`

---

## 使用自定義域名（選配）

### 前置準備
- 已擁有域名（如 `yourdomain.com`）
- 可訪問域名的 DNS 設置面板

### 方案 A: 使用子域名（推薦）

**優點**: 設置簡單、支援 CDN、不影響郵件服務

#### 1. DNS 設置（在域名商後台）

添加 CNAME 記錄：
```
類型: CNAME
名稱: www（或其他子域名，如 game）
值: 你的帳號.github.io
TTL: 自動或 3600
```

#### 2. GitHub Pages 設置

1. Repository **Settings** > **Pages**
2. **Custom domain** 輸入: `www.yourdomain.com`
3. 點擊 **Save**
4. 等待 DNS 檢查通過（可能需要幾分鐘到 24 小時）
5. 勾選 **Enforce HTTPS**（DNS 生效後）

### 方案 B: 使用根域名

**注意**: 可能影響郵件服務，請謹慎使用

#### 1. DNS 設置（在域名商後台）

添加 4 個 A 記錄：
```
類型: A
名稱: @
值: 185.199.108.153
TTL: 自動或 3600
```

重複添加其他 3 個 IP：
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

（可選）添加 www 的 CNAME：
```
類型: CNAME
名稱: www
值: 你的帳號.github.io
```

#### 2. GitHub Pages 設置

1. Repository **Settings** > **Pages**
2. **Custom domain** 輸入: `yourdomain.com`
3. 點擊 **Save**
4. 等待 DNS 檢查通過
5. 勾選 **Enforce HTTPS**

### DNS 生效時間

- 通常 10 分鐘到 1 小時
- 最長可能需要 24-48 小時
- 使用 `dig` 或線上工具檢查：
  ```bash
  dig www.yourdomain.com
  ```

### 常見問題

**Q: DNS 檢查失敗？**
- 確認 DNS 記錄正確
- 等待 DNS 傳播完成
- 清除瀏覽器快取

**Q: HTTPS 無法啟用？**
- 等待 DNS 完全生效
- 確認域名指向正確
- 24 小時後重試

**Q: 使用根域名後郵件無法收發？**
- 改用子域名方案（www）
- 或在 DNS 中正確配置 MX 記錄

---

## BGM 背景音樂設置

遊戲需要手動下載音樂檔案：

1. 前往 https://pixabay.com/music/search/chinese%20new%20year/
2. 選擇喜歡的中國新年音樂
3. 點擊「Free Download」下載 MP3
4. 重新命名為 `bgm.mp3`
5. 放置到專案的 `music/bgm.mp3`

> 若未放置音樂檔案，遊戲仍可正常遊玩，只是沒有背景音樂。
> 詳見 `music/README.md`。

## 本地測試

使用任何 HTTP 伺服器：
```bash
python3 -m http.server 8000
# 或
npx serve
```

訪問 `http://localhost:8000`

---

## 📄 授權與致謝

- **專案授權**: MIT License（見 [LICENSE](LICENSE)）
- **第三方資源**: 詳見 [CREDITS.md](CREDITS.md)
- **音樂來源**: Pixabay (CC0)
- **UI 框架**: Tailwind CSS (MIT)

---

## 🎮 遊戲特色

- ✨ 粒子系統（跳躍、收集、爆炸特效）
- 🎯 連擊系統與分數倍增
- 🌄 視差滾動背景
- 📱 移動端優化（觸控、暫停按鈕）
- 🎵 背景音樂系統
- 🎨 緩動動畫與螢幕震動
- ⚡ 性能優化（物件池、離屏 Canvas）

---

**Made with ❤️ for 馬年新春**
