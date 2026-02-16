# Pause System & Audio Fix Specification

## Scenario 1: 遊戲暫停功能

### Given: 遊戲正在進行中 (gameState === 'PLAYING')
### When: 玩家按下 P 鍵或 ESC 鍵
### Then: 
- 遊戲狀態切換為 'PAUSED'
- 顯示暫停覆蓋層
- 遊戲邏輯停止更新
- 再次按下恢復遊戲

## Scenario 2: 修復跳躍音效

### Given: 跳躍音效在 Audio.jump() 中定義
### When: 玩家跳躍時調用 jumpPlayer()
### Then: 
- 確保 Audio.jump() 被正確調用
- 音效正常播放

## Technical Requirements
- 暫停鍵：P 或 ESC
- 暫停畫面：半透明覆蓋層 + 提示文字
- 暫停時停止所有遊戲邏輯更新
- 保持渲染循環運行（顯示靜止畫面）
- 音效系統正常工作
