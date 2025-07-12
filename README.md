# Volcengine SDK Wheel

[English](#english) | [中文](#chinese)

<a name="english"></a>
## English

This project automatically builds and releases wheel packages for Volcengine SDK (https://github.com/volcengine/volc-sdk-python), providing pre-built packages for easy installation.

### Features

- **Universal Wheel Package**: Single wheel package supporting all Python versions
- **Automatic Version Detection**: Daily checks for new SDK releases
- **Manual Build Support**: Build specific versions on demand
- **GitHub Release Integration**: Automatically creates releases with wheel packages
- **Version Consistency**: Release tags match source code versions

### How It Works

#### Automatic Daily Builds
- Runs daily at 2:00 AM UTC (10:00 AM Beijing time)
- Checks for new versions in the official Volcengine SDK repository
- Automatically builds and releases if a new version is found
- Skips if the version has already been released

#### Manual Builds
- Trigger manually via GitHub Actions
- Specify any version tag to build
- Useful for testing or building specific versions

### Usage

1. **Download from Releases**: Visit the [Releases page](https://github.com/zhangp365/volcengine-wheel/releases) to download wheel packages
2. **Install with pip**: `pip install volcengine-xxx-py3-none-any.whl`
3. **Manual Build**: Go to Actions tab and trigger "Build and Release Wheels" workflow

### Supported Versions

- All Python versions (universal wheel)
- Latest Volcengine SDK releases

---

<a name="chinese"></a>
## 中文

这个项目自动构建并发布火山引擎SDK (https://github.com/volcengine/volc-sdk-python) 的wheel包，提供预构建的安装包以便于使用。

### 功能特性

- **通用Wheel包**: 单个wheel包支持所有Python版本
- **自动版本检测**: 每日检查SDK新版本发布
- **手动构建支持**: 按需构建指定版本
- **GitHub Release集成**: 自动创建包含wheel包的发布
- **版本一致性**: 发布标签与源代码版本保持一致

### 工作原理

#### 自动每日构建
- 每天UTC时间凌晨2点（北京时间上午10点）运行
- 检查官方火山引擎SDK仓库的新版本
- 发现新版本时自动构建并发布
- 如果版本已发布则跳过

#### 手动构建
- 通过GitHub Actions手动触发
- 可指定任意版本标签进行构建
- 适用于测试或构建特定版本

### 使用方法

1. **从Releases下载**: 访问 [Releases页面](https://github.com/zhangp365/volcengine-wheel/releases) 下载wheel包
2. **使用pip安装**: `pip install volcengine-xxx-py3-none-any.whl`
3. **手动构建**: 前往Actions标签页，触发"Build and Release Wheels"工作流

### 支持的版本
- 所有Python版本（通用wheel包）
- 最新的火山引擎SDK发布版本



### 技术细节

- **构建环境**: Windows Latest (GitHub Actions)
- **Python版本**: 3.9 (用于构建)
- **构建工具**: setuptools, wheel, build
- **触发方式**: 定时调度 + 手动触发
- **版本检查**: 通过GitHub API检查已发布的版本


