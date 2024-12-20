# 基于STM32F1和MLX90640的红外热像仪项目

## 项目简介

本项目展示了如何利用STM32F103RCT6单片机结合MLX90640红外传感器，搭建一个简易的红外热像仪系统。通过I2C接口，STM32F1能够高效地从MLX90640传感器获取温度数据，并在LCD屏幕上以像素点的形式显示热分布图。系统具备温度超标报警功能，当检测到温度超出预设值时，内置的蜂鸣器会自动响起，且可通过按键手动解除报警。

## 主要特点

- **传感器**: MLX90640，具有32x24像素的分辨率，提供了精确的非接触式温度测量。
- **控制芯片**: STM32F103RCT6，负责数据处理和系统控制。
- **显示**: LCD屏幕用于实时展示热像结果，包括温度值和视觉化的热图。
- **交互**: 设有按键，用于设定温度阈值和控制报警。
- **功能**: 自动温度检测、报警机制、手动报警消除。

## 工作流程

1. **初始设置**: 上电后，MLX90640内部完成初始化。
2. **数据采集**: 通过I2C协议周期性读取传感器数据，每秒2次数据刷新。
3. **温度处理**: 实时数据转换为温度值，生成对应的伪彩色图像。
4. **显示**: 将处理后的温度数据映射为像素值，在LCD屏幕上形成热像图。
5. **报警**: 温度过高时激活蜂鸣器，通过按键可静音。

## 注意事项

- 由于未采用阵列插值处理，所得图像可能会有锯齿现象。
- 资源包括完整的Keil程序和接线图，适用于学习和项目参考。
- 提供的源码未经双线性插值处理，用户可根据需求进行优化，以提升图像平滑度。

## 获取资源

源码及相关文档可从提供的链接下载，确保遵守CC 4.0 BY-SA版权协议，正确署名并在二次分享时附上原始来源链接。

---

此项目适合单片机爱好者、嵌入式开发者以及对红外热成像技术感兴趣的工程师进行研究和实践。通过本项目的学习，您将能够掌握如何结合特定传感器与STM32系列单片机进行复杂系统的开发。

## 下载链接

[基于STM32F1和MLX90640的红外热像仪项目](https://pan.quark.cn/s/a05d50c407c0)