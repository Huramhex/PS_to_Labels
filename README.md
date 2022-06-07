PS_to_Labels
====
Transform PS images to masks for semantic segmentation

https://codeantenna.com/a/hZypo7ZQHu

图片格式
------
- 图像 → 模式 → RGB颜色 → 8位/通道
- 图层 → 新建 → 图层背景（背景色纯黑）
  - 确保图片为3通道
- 保存为.PNG

使用工具
--------
- 多边形套索工具
  - ![[多边形](https://github.com/Huramhex/PS_to_Labels/blob/292bb7a5a066d03d788ffe60d7b36d927813aba2/ps_to_masks/%E5%A4%9A%E8%BE%B9%E5%A5%97%E7%B4%A2.png)](https://github.com/Huramhex/image/blob/154606d57fb72b0b413412531d3f329f2daab36b/ps_to_masks/%E5%A4%9A%E8%BE%B9%E5%A5%97%E7%B4%A2.png)
  - 设置羽化0 不勾选消除锯齿，否则会出现过度色，后面可以用套索进行多边形标注。套索和矩形选框工具是不会产生过度色的。
- 魔棒工具
  - ![mobang](https://github.com/Huramhex/image/blob/154606d57fb72b0b413412531d3f329f2daab36b/ps_to_masks/%E9%AD%94%E6%9C%AF%E6%A3%92.png)
  - 除魔棒以外的其他工具会出现过渡色

填充颜色
--------
- ![yanse](https://github.com/Huramhex/image/blob/154606d57fb72b0b413412531d3f329f2daab36b/ps_to_masks/%E8%89%B2%E6%9D%BF.png)
- 选择区域，填充色板中RGB颜色
- 合并图层 → 图层 → 新建 → 图层背景（背景色纯黑）
  - 透明色有一定概率出现问题，不建议使用 

输出PS图片
-----
- 图像 → 模式 → RGB颜色 → 8位/通道
- .PNG

制作colormap
------
- 新建文档，RGB为8位
- ![xinjian](https://github.com/Huramhex/image/blob/10582de2dd33166d11bf403c7f761f6cef1902db/ps_to_masks/colormap%E6%96%B0%E5%BB%BA.png)
- 制作一个纯色的colormap，将自己标注的颜色都存进去（黑色得放进去，注意图片一定得是纯色没有过渡色的）
- ![colormap](https://github.com/Huramhex/PS_to_Labels/blob/351a8986263438af855a7adbd4a2e54e2d4425e8/colormap/colormap.png)
- 导出为.PNG

转换为masks
-----
- PS图片放入文件夹 '.\masks'
- colormap放入文件夹 '.\colormap'
- 运行程序，新label图片直接覆盖原图片输出

