# BGM System Implementation

## Scenario: 遊戲背景音樂

### Given: 遊戲需要歡樂的年節氛圍
### When: 遊戲開始時
### Then: 
- 播放循環的中國新年 BGM
- 音量適中不干擾音效
- 暫停時停止 BGM
- 恢復時繼續播放
- 遊戲結束時繼續播放（歡樂氛圍）

## Audio Source
- Platform: Pixabay (CC0 License)
- Tracks:
  1. Chinese New Year (ID: 187532) - 傳統樂器、打擊樂
  2. Chinese New Year (ID: 284910) - 廣告風格、亞洲音樂
  3. Chinese New Year (ID: 4544) - 優雅、振奮

## Technical Requirements
- 使用 HTML5 Audio 元素
- 循環播放 (loop)
- 音量控制 (0.3-0.5)
- 暫停/恢復控制
- 首次互動後自動播放（瀏覽器政策）
- 提供音樂來源歸屬

## Implementation
- 添加 <audio> 元素到 HTML
- 使用 Pixabay CDN 直連（如可用）或提示用戶下載
- 在 startGame() 時播放
- 在 togglePause() 時控制
- 添加音樂歸屬到頁面
