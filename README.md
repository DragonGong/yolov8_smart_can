# Intelligent Household Garbage Bin (YOLOv8)

本项目为 **中国大学生工程实践与创新能力大赛（工训赛）** 的智能家居垃圾桶方案，基于 YOLOv8 进行垃圾视觉识别，并集成了多垃圾检测、满载检测和大模型语音交互模块。

> 致谢：视觉检测框架基于 Ultralytics YOLOv8 开源项目实现。

---

## 项目概览

- **核心能力**
  - 垃圾图像识别与分类
  - 多目标垃圾识别（同一画面多个垃圾）
  - 满载状态检测
- **适用场景**
  - 工训赛作品演示
  - 智能垃圾桶原型验证


---

## 快速导航

- 中文说明（更详细）：[`README.zh-CN.md`](README.zh-CN.md)
- 视觉相关核心代码：`classify.py`、`various_classify.py`、`full_inspection.py`、`nano/various_cv.py`、`nano/yolo_module.py`
- UI 与设备联调：`nano/UI.py`、`nano/test_send.py`、`nano/test_recv.py`

---

## 目录结构（nano）

```text
nano/
├── AI_module.py
├── IFlytek.py
├── SparkApi.py
├── UI.py
├── cv_module.py
├── docs/
│   ├── answers.txt
│   ├── keywords.txt
│   └── questions.txt
├── img/
├── inspector.py
├── lock.py
├── test_recv.py
├── test_send.py
├── various_cv.py
├── voice/
├── voice_assitant/
└── yolo_module.py
```

---

## 关键脚本说明

### 根目录脚本

- `classify.py`：单个垃圾分类。
- `various_classify.py`：多个垃圾同时分类。
- `full_inspection.py`：满载检测逻辑。

### `nano/` 目录脚本

- `nano/various_cv.py`：多目标视觉流程。
- `nano/yolo_module.py`：YOLO 推理封装模块。
- `nano/UI.py`：界面展示与交互逻辑。
- `nano/cv_module.py`：早期视觉代码。

---

## 补充资源

- 演示视频（YouTube）：<https://www.youtube.com/watch?v=mjIxYqITBE4>
- 摄像头曝光调节参考：<https://blog.csdn.net/m0_63230414/article/details/133394588>

---

## 说明

当前仓库同时包含 Ultralytics 上游代码与项目自定义代码。若你只关注比赛作品实现，建议优先从以下路径开始阅读：

1. `classify.py` / `various_classify.py` / `full_inspection.py`
2. `nano/various_cv.py` / `nano/yolo_module.py`
3. `nano/UI.py`

