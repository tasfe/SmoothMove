## 使用高德地图实现点平滑移动 - 优化版

### 1. 原有方案介绍
之前有写过一篇 [使用高德地图模拟运动轨迹](http://facex.xyz/2016/12/14/%E4%BD%BF%E7%94%A8%E9%AB%98%E5%BE%B7%E5%9C%B0%E5%9B%BE%E6%A8%A1%E6%8B%9F%E8%BF%90%E5%8A%A8%E8%BD%A8%E8%BF%B9/), 介绍了使用高德地图的点平滑移动 API 来实现模拟运动轨迹，但是存在几个问题：
1. 一旦设置了动画时间并开始动画，只有停止选项，然后就没有然后了。
2. 不支持在轨迹上任意位置暂停，高德 API 的动画只能在 ** 轨迹的经纬度数组中的点 ** 停止，当调用停止动画时，而点还没有到达经纬度数组中的点的位置，这时点会继续向前走（而不是马上停止），直到到达数组中下一个经纬度点上。
3. 不支持以速度来驱动动画，并在动画过程中改变速度。

### 2. 优化方案介绍
针对上面的 3 个问题，本次分享的点平滑移动方案优化如下：

1. 支持暂停和继续。
2. 支持在任意时刻，任意位置暂停。
3. 支持以速度来驱动动画，并且支持动画中改变速度。
---
## 更多请查看博客:[使用高德地图实现点平滑移动-优化版](http://facex.xyz/2017/06/06/使用高德地图实现点平滑移动-优化版/)
