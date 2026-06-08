# MdLock Viewer

即時 Markdown 預覽 × AES-256-GCM 加密文件閱讀。純前端，無後端，無伺服器。

🔗 **Live** → https://wenhsi.github.io/mdlock-viewer/

---

## 功能

- **即時 Markdown 預覽**：左側編輯，右側同步渲染
- **加密文件閱讀**：開啟 MdLock Encryptor 產生的分享連結，輸入密碼即解密
- **支援 URL 參數**：`?gist=<id>` 直接載入指定 Gist
- **深色 / 淺色主題**：偏好設定儲存於 localStorage
- **完整 RWD**：桌面分割畫面，手機切換編輯 / 預覽

---

## 使用方式

### 一般 Markdown 編輯預覽

直接開啟頁面，在左側輸入 Markdown，右側即時渲染結果。

### 閱讀加密文件

1. 開啟 MdLock Encryptor 產生的分享連結（含 `?gist=` 參數）
2. 頁面自動偵測並顯示解密表單
3. 輸入加密時設定的密碼，點擊解密
4. 解密成功後即顯示 Markdown 渲染結果

---

## 技術

| 項目 | 說明 |
|------|------|
| 解密 | Web Crypto API — AES-256-GCM |
| 金鑰派生 | PBKDF2（SHA-256，100,000 次迭代） |
| Gist 讀取 | GitHub Gist API v3（公開，無需 Token） |
| 架構 | 純 HTML / CSS / JS，單檔，無框架，無依賴 |

---

## 相關

- [MdLock Encryptor](https://wenhsi.github.io/mdlock-encryptor/) — 加密並上傳文件

## License

MIT © 2026 wenhsi
