# 可复现Meta分析项目
本项目为可复现Meta分析研究，基于R语言实现，使用 `renv` 锁定完整运行环境，确保所有人均可一键复现完全一致的分析结果。

## 小组成员
- 师 &nbsp; &nbsp;鑫 2025303120092 [@hzauShixin](https://github.com/hzauShixin)  
- 陈 &nbsp; &nbsp;浩 2025303110111 [@haochen-co](https://github.com/haochen-co)
- 梅 &nbsp; &nbsp;良 2025303120116 [@shi-mlml](https://github.com/shi-mlml)
- 陈 &nbsp; &nbsp;希 2025303110109 [@Doloressss770](https://github.com/Doloressss770)
- 杨瑀珩 2025303110100 [@logicyyh](https://github.com/logicyyh)

## 项目结构说明
- `data/`: 存放项目原始数据文件
- `code/`: 存放分析代码（Rmd文件）
- `outputs/`: 存放分析生成的图片和HTML报告
- `renv/`: R环境管理文件夹，用于复现项目环境

## 研究背景
经典“入侵悖论”认为：本地物种与外来物种丰富度的关系（NERR）在**小空间尺度呈负相关**（生物抵抗），在**大空间尺度呈正相关**（环境异质性）。
Peng et al. (2019) 通过全球 101 篇文献、204 个案例的**分层混合效应元分析**首次严格检验该假说，发现：
1. NERR 随取样面积（grain）增大而显著增强，但**在任何尺度上平均均为正相关**，不支持传统入侵悖论。
2. 空间范围（extent）对 NERR 影响较弱，grain 是主导因素。
3. NERR 随纬度升高而增强，并受经度影响呈二次格局。
4. 现有研究高度集中于北美与西欧，热带与极地数据严重不足。

## 本项目复现目标
1. 复现论文核心元分析流程：Fisher’s z 转换、混合效应模型、尺度效应检验。
2. 复现关键图表：grain 与 effect size 关系、纬度/经度格局、生境与 extent 分组结果。
3. 实现完整可复现的分析流程，使用 R Markdown + renv 保证环境一致性。
4. 复现并验证论文对“入侵悖论”的核心结论。

## 📁 项目文件说明
- `wzfx.Rmd`：核心分析代码（Meta分析完整流程）
- `DataS2_MetaAnalysisDatabase.csv`：研究原始数据集
- `renv.lock` / `renv/`：环境锁定文件（保证依赖版本一致）
- `.Rprofile`：项目环境自动配置文件
- 图片文件（Fig.1.png / Fig.2B.png / Fig.S1.png）：复现结果可视化图表

## 🚀 一键复现步骤
### 1. 克隆/下载本项目到本地
### 2. 使用RStudio打开项目（双击 `wzfx.Rproj`）
### 3. 恢复完整运行环境
```r
# 安装renv（未安装时执行）
install.packages("renv")
# 自动恢复所有依赖包（精确匹配环境）
renv::restore()
```

### 4. 运行核心代码
打开 wzfx.Rmd，点击 Run All 即可完整复现所有分析结果与图表
