# 计算器应用工程文件描述

## 项目概述

这是一个基于HarmonyOS ArkTS开发的计算器应用项目，使用HarmonyOS SDK 5.0.5(17)构建。项目名称为"arktscalc"，版本为1.0.0。

## 项目结构

### 根目录结构
```
calculator-master/
├── .appanalyzer/                    # 应用分析器配置目录
│   └── appanalyzerCardConfig/       # 卡片配置
│       ├── appTestCardList.json     # 应用测试卡片列表
│       ├── atomicServiceTestCardList.json  # 原子服务测试卡片列表
│       └── defaultCardVersion.txt   # 默认卡片版本
├── .hvigor/                         # Hvigor构建系统缓存和输出
│   ├── cache/                       # 构建缓存
│   ├── dependencyMap/               # 依赖映射
│   ├── outputs/                     # 构建输出
│   └── report/                      # 构建报告
├── .idea/                           # IDE配置文件
│   └── .deveco/                     # DevEco Studio配置
├── AppScope/                        # 应用全局配置
│   └── resources/                   # 全局资源
│       └── base/
│           ├── element/             # 元素定义
│           │   └── string.json      # 字符串资源
│           └── media/               # 媒体资源
│               └── app_icon.png     # 应用图标
├── entry/                           # 主模块
│   ├── build/                       # 构建目录
│   ├── src/                         # 源代码
│   │   └── main/                    # 主代码目录
│   │       ├── ets/                 # ArkTS源代码
│   │       │   ├── calc/            # 计算器相关代码
│   │       │   │   └── pages/       # 计算器页面
│   │       │   │       └── CardCalc.ets  # 卡片计算器组件
│   │       │   ├── entryability/    # 入口能力
│   │       │   │   └── EntryAbility.ets  # 入口能力组件
│   │       │   ├── entryformability/ # 表单能力
│   │       │   │   └── EntryFormAbility.ets  # 表单能力组件
│   │       │   ├── model/           # 模型层
│   │       │   │   └── Logger.ts    # 日志工具
│   │       │   └── pages/           # 页面
│   │       │       └── Index.ets    # 主页面组件
│   │       └── resources/           # 模块资源
│   │           ├── base/            # 基础资源
│   │           │   ├── element/     # 元素定义
│   │           │   │   ├── color.json      # 颜色定义
│   │           │   │   ├── float.json      # 浮点数定义
│   │           │   │   └── string.json     # 字符串资源
│   │           │   ├── media/       # 媒体资源
│   │           │   │   ├── checked.png     # 选中图标
│   │           │   │   ├── equal.png       # 等号图标
│   │           │   │   ├── icon.png        # 图标
│   │           │   │   ├── ic_back.png     # 返回图标
│   │           │   │   ├── ic_cal_delete.svg    # 删除图标
│   │           │   │   ├── ic_cal_delete_c.svg  # C删除图标
│   │           │   │   ├── ic_cal_division.svg  # 除法图标
│   │           │   │   ├── ic_cal_eight.svg     # 数字8图标
│   │           │   │   ├── ic_cal_equal.svg     # 等号图标
│   │           │   │   ├── ic_cal_five.svg      # 数字5图标
│   │           │   │   ├── ic_cal_four.svg      # 数字4图标
│   │           │   │   ├── ic_cal_minus.svg     # 减号图标
│   │           │   │   ├── ic_cal_multiply.svg  # 乘号图标
│   │           │   │   ├── ic_cal_nine.svg      # 数字9图标
│   │           │   │   ├── ic_cal_one.svg       # 数字1图标
│   │           │   │   ├── ic_cal_percent.svg   # 百分号图标
│   │           │   │   ├── ic_cal_plus.svg      # 加号图标
│   │           │   │   ├── ic_cal_point.svg     # 小数点图标
│   │           │   │   ├── ic_cal_seven.svg     # 数字7图标
│   │           │   │   ├── ic_cal_six.svg       # 数字6图标
│   │           │   │   ├── ic_cal_three.svg     # 数字3图标
│   │           │   │   ├── ic_cal_two.svg       # 数字2图标
│   │           │   │   ├── ic_cal_zero.svg      # 数字0图标
│   │           │   │   ├── ic_hop.svg           # 跳转图标
│   │           │   │   ├── ic_hop_normal.png    # 跳转正常图标
│   │           │   │   └── uncheck.png          # 未选中图标
│   │           │   └── profile/     # 配置文件
│   │           │       ├── form_config.json    # 表单配置
│   │           │       └── main_pages.json     # 主页面配置
│   │           ├── en_US/           # 英文资源
│   │           │   └── element/
│   │           │       └── string.json
│   │           └── zh_CN/           # 中文资源
│   │               └── element/
│   │                   └── string.json
│   └── module.json5                 # 模块配置文件
├── hvigor/                          # Hvigor配置
│   └── hvigor-config.json5          # Hvigor配置文件
├── screenshots/                     # 截图目录
├── build-profile.json5              # 构建配置文件
├── hvigorfile.ts                    # Hvigor构建脚本
└── oh-package.json5                 # 项目包配置文件
```

## 核心文件说明

### 1. 配置文件

#### `build-profile.json5` (根目录)
- **作用**: 项目构建配置文件
- **内容**: 定义应用签名配置、产品配置、模块配置
- **关键配置**:
  - 兼容SDK版本: 5.0.5(17)
  - 目标SDK版本: 5.0.5(17)
  - 运行时操作系统: HarmonyOS
  - 模块: entry模块

#### `oh-package.json5` (根目录)
- **作用**: 项目包配置文件
- **内容**: 
  - 项目名称: arktscalc
  - 版本: 1.0.0
  - 模型版本: 5.0.0
  - 依赖: 当前无外部依赖

#### `hvigorfile.ts` (根目录)
- **作用**: Hvigor构建脚本
- **内容**: 导入HarmonyOS构建插件

### 2. 模块配置文件

#### `entry/src/main/module.json5`
- **作用**: 模块配置
- **关键配置**:
  - 模块名称: entry
  - 模块类型: entry (入口模块)
  - 设备类型: phone (手机)
  - 主元素: EntryAbility
  - 页面: pages/Index
  - 能力:
    - EntryAbility: 入口能力，支持系统主页启动
    - EntryFormAbility: 表单能力，支持卡片形式

### 3. 源代码文件

#### `entry/src/main/ets/pages/Index.ets`
- **作用**: 计算器主页面组件
- **功能**:
  - 实现计算器UI界面
  - 包含5行按钮布局
  - 支持数字输入、运算符输入
  - 支持清除(C)、删除(←)、等号(=)操作
  - 实时显示表达式和计算结果
- **技术特点**:
  - 使用ArkTS声明式UI
  - 使用@State管理状态
  - 使用LocalStorage进行状态持久化
  - 使用ForEach循环渲染按钮

#### `entry/src/main/ets/calc/pages/CardCalc.ets`
- **作用**: 卡片计算器组件
- **功能**: 与主页面类似的计算器功能，用于卡片形式展示

#### `entry/src/main/ets/entryability/EntryAbility.ets`
- **作用**: 入口能力组件
- **功能**: 应用启动入口，管理应用生命周期

#### `entry/src/main/ets/entryformability/EntryFormAbility.ets`
- **作用**: 表单能力组件
- **功能**: 提供卡片形式的计算器功能

#### `entry/src/main/ets/model/Logger.ts`
- **作用**: 日志工具类
- **功能**: 提供debug、info、warn、error等日志级别
- **依赖**: @kit.PerformanceAnalysisKit

### 4. 资源文件

#### 图标资源 (`entry/src/main/resources/base/media/`)
- 数字图标: ic_cal_zero.svg 到 ic_cal_nine.svg
- 运算符图标: ic_cal_plus.svg, ic_cal_minus.svg, ic_cal_multiply.svg, ic_cal_division.svg
- 功能图标: ic_cal_delete.svg, ic_cal_delete_c.svg, ic_cal_equal.svg, ic_cal_percent.svg, ic_cal_point.svg
- 其他图标: ic_back.png, ic_hop.svg, checked.png, uncheck.png

#### 配置文件 (`entry/src/main/resources/base/profile/`)
- `main_pages.json`: 定义主页面为pages/Index
- `form_config.json`: 表单配置

#### 字符串资源
- `AppScope/resources/base/element/string.json`: 应用全局字符串
- `entry/src/main/resources/base/element/string.json`: 模块字符串
- 多语言支持: en_US, zh_CN

### 5. 构建系统文件

#### `hvigor/hvigor-config.json5`
- **作用**: Hvigor构建配置

#### `entry/build-profile.json5`
- **作用**: 模块构建配置
- **配置**: API类型为stageMode，包含default和ohosTest两个构建目标

## 技术架构

### 架构模式
- **UI层**: ArkTS声明式UI组件
- **业务逻辑层**: 计算器核心逻辑
- **数据层**: LocalStorage状态管理
- **工具层**: Logger日志工具

### 关键技术
1. **ArkTS**: HarmonyOS应用开发语言
2. **声明式UI**: 使用@Entry、@Component等装饰器
3. **状态管理**: 使用@State装饰器管理组件状态
4. **本地存储**: 使用LocalStorage进行状态持久化
5. **资源管理**: 多语言、多分辨率资源支持

### 计算器功能
1. **基本运算**: 加(+)、减(-)、乘(*)、除(/)
2. **数字输入**: 0-9数字输入
3. **特殊功能**: 
   - 清除(C): 清空表达式和结果
   - 删除(←): 删除最后一个字符
   - 等号(=): 计算结果
   - 小数点(.): 小数输入
   - 百分号(%): 百分比计算

## 构建和运行

### 构建工具
- **Hvigor**: HarmonyOS构建工具
- **构建模式**: stageMode

### 运行环境
- **SDK版本**: 5.0.5(17)
- **目标设备**: 手机
- **操作系统**: HarmonyOS

## 项目特点

1. **模块化设计**: 清晰的目录结构，分离UI、业务逻辑和工具
2. **多语言支持**: 支持中文和英文
3. **多分辨率适配**: 提供多种图标资源
4. **卡片支持**: 支持表单卡片形式展示
5. **日志系统**: 完整的日志记录功能
6. **状态管理**: 使用LocalStorage进行状态持久化

## 文件统计

- **配置文件**: 8个
- **源代码文件**: 5个 (.ets, .ts)
- **资源文件**: 30+个 (图片、图标、字符串等)
- **构建文件**: 多个缓存和配置文件

## 依赖关系

### 内部依赖
- `Index.ets` → `calc()` 函数 (计算逻辑)
- `Index.ets` → `calcButtonX()` 函数 (按钮配置)
- `Index.ets` → `isOperator()` 函数 (运算符判断)

### 外部依赖
- `@kit.PerformanceAnalysisKit`: 性能分析工具包 (用于日志)

## 注意事项

1. 项目使用HarmonyOS ArkTS开发，需要HarmonyOS开发环境
2. 构建需要Hvigor工具
3. 需要HarmonyOS SDK 5.0.5(17)或更高版本
4. 支持手机设备运行
5. 支持卡片形式展示计算器功能