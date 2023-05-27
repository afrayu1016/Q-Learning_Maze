# Q-Learning_Maze

## Context
Using Q-learining or any reinforcement learning algorithm to find out the way to escape the maze.
## Rules
* 迷宮本身為21*11的迷宮，起點左上角(0,0) 終點為右下角(20,10)，移動時不可穿過障礙物
  - X表示牆壁位置(顏色為綠色方便區分) 
  - O表示寶藏位置(顏色為橘色方便區分) 
  - S表示起點位置 
  - G表示終點位置 
  - 黃色底色表示可能路徑

* 寶藏計分方式為參數Score，每踩到一個寶箱Score+1 每場重置 每回合都必須計算Score分數 最高5分

## Implementaion
* 設定x,y軸長度，40*30的無障礙迷宮
* 設定可行動動作為上下左右，目標位置在最右下角
* 設計Reward
  - 設定Action方向，若為右或下，則Reward正常
  - 設定Action方向，若為右或下，則Reward較高
  - 設定SCORE為計算寶藏分數用，則Reward較高
  - 若走到牆壁，或是往回走的情況下，則扣除Reward

