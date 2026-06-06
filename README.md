# Hi, I'm Teddy Yang

Computer Vision / Systems / Audio ML developer at Southern University of Science and Technology, Shenzhen.

I build reproducible research pipelines, performance-oriented C++ systems, and ML infrastructure that can be tested, benchmarked, and explained from code to result.

## Focus Areas

- Computer vision and 3D scene understanding: 3D Gaussian Splatting, object segmentation, OpenCV, reconstruction workflows.
- Systems engineering: C++ order-management systems, replay engines, risk checks, deterministic testing, low-latency design tradeoffs.
- ML and signal processing infrastructure: audio feature extraction, keyword spotting, ONNX export, structured inference outputs.
- Quantitative research tooling: data ingestion, factor research, walk-forward evaluation, backtesting, and report generation.

## Featured Projects

### OpenCV Contributions

[opencv/opencv fork](https://github.com/Teddy-Yangjiale/opencv) | C++ | Computer Vision | Performance Optimization

Contributed patches to OpenCV, including RISC-V RVV optimization paths, DNN activation vectorization, and video I/O / build fixes.

- Worked on universal intrinsics and RISC-V RVV paths for selected core operations.
- Optimized DNN sigmoid activation kernels with vectorized implementations.
- Fixed platform-specific videoio and build issues.
- Practiced upstream-style engineering: scoped PRs, review feedback, CI awareness, and portability constraints.

Related upstream PRs include `opencv/opencv#29058`, `#29057`, `#29033`, `#28999`, `#28914`, and `#28894`.

### 3DGS Object Segmentation

[3DGS](https://github.com/Teddy-Yangjiale/3DGS) | Shell / Python workflows | Computer Vision | 3D Gaussian Splatting

Reproducible project for object-level segmentation and editing in 3D Gaussian Splatting, focused on Gaussian Grouping over LERF-MASK scenes.

- Built server-side experiment workflow for training, rendering, and evaluation.
- Reproduced LERF-MASK scenes: `figurines`, `ramen`, and `teatime`.
- Documented environment setup, dataset layout, experiment protocol, bottleneck analysis, and downstream editing.
- Reported quantitative results, including Mean IoU / Boundary IoU for baseline and enhanced experiments.

### Quant System

[quant](https://github.com/Teddy-Yangjiale/quant) | Python | Quant Research | Backtesting

A reproducible quantitative research system for data ingestion, factor research, walk-forward evaluation, backtesting, reporting, and simulated trading interfaces.

- Supports Yahoo Finance and A-share data workflows with local Parquet storage.
- Implements factor analysis, IC / RankIC evaluation, vectorized and ledger-style backtesting.
- Uses walk-forward evaluation to reduce sample-in overfitting.
- Includes research reports, strategy runners, testing hooks, and CI-oriented commands.

### HFT MVP

[HFT](https://github.com/Teddy-Yangjiale/HFT) | C++ | Trading Systems | Deterministic Replay

A staged C++ high-frequency trading system prototype focused on market replay, order book updates, order management, pre-trade risk, and paper execution.

- Implemented CSV market-data replay, level-2 order book top-of-book maintenance, and strategy interfaces.
- Added OMS lifecycle handling, cancel / cancel-replace workflows, execution ID deduplication, and fill simulation.
- Built risk hardening features: exposure tracking, rate limits, global and symbol kill switches.
- Added raw packet journaling, normalized event replay, sequence gap detection, and snapshot recovery APIs.
- Kept project boundaries explicit: research prototype, deterministic tests, and documented gaps versus production trading systems.

### Audio Analyzer

[audio_analyzer](https://github.com/Teddy-Yangjiale/audio_analyzer) | C++17 | Signal Processing | CLI / HTTP Service

A C++ audio feature extraction tool with CLI and HTTP server modes, designed as a structured feature frontend for downstream ML pipelines.

- Extracts MFCC, filterbank, log-Mel, spectral, chroma, time-domain, VAD, pitch, and quality metrics.
- Produces structured JSON with metadata, frame-level features, summary statistics, and quality diagnostics.
- Provides `--legacy-array` compatibility for older training scripts.
- Uses CMake-based C++ architecture with source modules and tests.

### Audio Keyword Recognition

[audio_train](https://github.com/Teddy-Yangjiale/audio_train) | Python | PyTorch | Audio ML

Training pipeline for Google Speech Commands keyword recognition, connected with the C++ audio analyzer frontend.

- Supports ResNet, CNN, and MLP models.
- Includes MFCC / Delta / Delta-Delta feature handling, SpecAugment, class weights, label smoothing, early stopping, checkpoint resume, and gradient clipping.
- Provides evaluation, confusion matrix visualization, t-SNE visualization, single-file inference, and ONNX export.
- Also includes a bandwidth extension subproject for audio restoration experiments.

### CS307 DBMS Course Project

[Sustech_CS307_Course_Project](https://github.com/Teddy-Yangjiale/Sustech_CS307_Course_Project) | Java | Database Systems

Course-scale database system project covering SQL execution, indexing, transaction behavior, and storage-oriented design.

- Built around planner / executor style database components.
- Includes B+Tree indexing validation and performance experiments.
- Implements transaction-related workflows such as rollback-oriented runtime state handling and savepoint-style behavior.
- Useful as a compact DBMS implementation for explaining system architecture from SQL input to physical execution.

### CVProject Indoor Reconstruction

[CVProject](https://github.com/Teddy-Yangjiale/CVProject) | Python | Computer Vision | 3D Reconstruction

Exploration project for indoor reconstruction workflows, including dataset triage and reconstruction bottleneck analysis.

- Investigated monocular reconstruction limitations under low parallax.
- Compared practical routes such as RGB-D fusion, dense MVS, learned dense SLAM, NeRF, and 3DGS-style methods.
- Emphasized honest diagnosis of reconstruction quality instead of treating sparse or unstable geometry as success.

## Tech Stack

Languages: C++, Python, Java, C, Shell, TypeScript  
Core tools: OpenCV, PyTorch, CMake, Git, Linux / WSL, CUDA-aware workflows, Maven, pytest, CTest  
Domains: Computer Vision, 3DGS, Audio ML, DBMS, Quant Research, Trading Systems

## Current Direction

I am especially interested in systems that connect research ideas with reliable engineering:

- CV and 3D reconstruction pipelines that are reproducible and measurable.
- Open-source performance work in mature C++ codebases.
- ML tooling that keeps data, features, models, and evaluation results auditable.
- Systems projects where correctness, latency, and testability matter together.

---

# 中文简介

我是 Teddy，目前在南方科技大学，主要关注 **计算机视觉、系统工程、音频机器学习和量化研究工具链**。

我更喜欢做能从代码一路解释到结果的项目：环境怎么搭、数据怎么流、实验怎么复现、指标怎么验证、系统边界在哪里，这些都应该能在项目里说清楚。

## 主要方向

- **计算机视觉 / 3D 重建**：3D Gaussian Splatting、Gaussian Grouping、OpenCV、室内重建与数据集分析。
- **C++ 系统工程**：订单簿、OMS、风控、回放、测试、低延迟系统设计。
- **音频与机器学习基础设施**：C++ 特征提取、Python 训练管线、关键词识别、ONNX 导出。
- **量化研究系统**：行情数据、因子研究、样本外 walk-forward、回测报告和模拟交易接口。

## 精选项目说明

- **OpenCV Contributions**：参与 OpenCV 上游贡献，涉及 RISC-V RVV 优化、DNN sigmoid 向量化、videoio / build 修复等。这是我目前最强的开源工程信号。
- **3DGS Object Segmentation**：围绕 Gaussian Grouping 和 LERF-MASK 做 3DGS 目标级分割复现，包含环境搭建、训练、渲染、评估、IoU 结果和实验文档。
- **Quant System**：一个面向量化研究的 Python 系统，覆盖数据更新、因子分析、walk-forward 样本外验证、回测和报告生成。
- **HFT MVP**：C++ 高频交易系统原型，包含市场数据回放、订单簿、OMS、风控、模拟撮合、网关抽象和确定性 replay。
- **Audio Analyzer / Audio Train**：C++ 音频特征提取器 + Python 关键词识别训练管线，覆盖 MFCC、log-Mel、VAD、F0、ResNet/CNN/MLP、SpecAugment 和 ONNX 导出。
- **CS307 DBMS Course Project**：Java 数据库课程项目，适合展示 SQL 执行、索引、事务和系统架构理解。
- **CVProject**：室内重建探索项目，重点不是包装结果，而是分析低视差视频为什么难以稳定重建，并比较更可靠的 RGB-D / MVS / SLAM / 3DGS 路线。

## 我希望继续深入的方向

- 可复现的 CV / 3D reconstruction 实验管线。
- 大型 C++ 开源项目中的性能优化和工程修复。
- ML 数据、特征、模型、评估结果之间可追踪的工具链。
- 同时重视正确性、性能和测试证据的系统项目。
