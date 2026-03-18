# 可复现Meta分析项目
本项目为可复现Meta分析研究，基于R语言实现，使用 `renv` 锁定完整运行环境，确保所有人均可一键复现完全一致的分析结果。

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
