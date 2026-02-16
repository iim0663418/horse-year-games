# Mobile Pause & Death Explosion Enhancement

## Scenario 1: 移動端暫停按鈕

### Given: 遊戲在移動端運行（無鍵盤）
### When: 玩家需要暫停遊戲
### Then: 
- HUD 區域顯示暫停按鈕（⏸ 圖示）
- 點擊按鈕切換暫停/恢復
- 按鈕位置不干擾遊戲操作
- 暫停時按鈕變為播放圖示（▶）

## Scenario 2: 死亡超級大爆炸

### Given: 玩家碰撞障礙物死亡
### When: 觸發 gameOver()
### Then: 
- 生成超級大爆炸粒子效果
- 粒子數量：150-200 個
- 多種顏色：紅、橙、黃、金、白
- 更大範圍：半徑 200-300px
- 更高速度：初速 8-15
- 更長持續時間：60-90 frames
- 螢幕強烈震動

## Technical Requirements
- 暫停按鈕：固定在 HUD 右上角
- 按鈕樣式：圓形、半透明背景、清晰圖示
- 爆炸效果：使用現有粒子系統擴展
- 性能：保持 60 FPS
