# BGM Playback Fix Specification

## Problem Diagnosis
- BGM URL 可能無效或需要認證
- 瀏覽器自動播放限制
- 音量設置問題

## Solution: 使用備用方案

### Option 1: 測試當前 URL
- 檢查 Pixabay CDN URL 是否可訪問

### Option 2: 使用本地音樂文件
- 提示用戶下載音樂到 music/ 目錄
- 更新 src 路徑

### Option 3: 使用其他 CDN
- 尋找可靠的 CDN 源

## Technical Requirements
- 確保 BGM 在首次用戶互動後播放
- 添加播放失敗的視覺反饋
- 提供音樂下載指引
