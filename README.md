# Game2048
Game 2048 implemented by javascript

这是一个用js实现的2048小游戏，核心思想是，对于上下左右4个方向的移动，统一将棋盘重心旋转至一个方向，用通用的移位函数操作元素，再将棋盘转回去。例如：

先实现一个`左->右`的移位函数 `toRight()`  
对于`左->右`：toRight()  
对于`右->左`：棋盘顺时针转180度，toRight()，棋盘逆时针转180度  
对于`上->下`：棋盘逆时针转90度，toRight()，棋盘顺时针转90度  
对于`下->上`：棋盘顺时针转90度，toRight()，棋盘逆时针转90度  
