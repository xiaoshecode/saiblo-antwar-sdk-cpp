# saiblo-antwar-sdk-cpp 维护说明

ANTWar 智能体比赛的 C++ SDK、模拟器和示例。

- 上游：https://github.com/saiblo/saiblo-antwar-sdk-cpp
- 在线文档：https://xiaoshecode.github.io/xiaoshecode/repos/saiblo-antwar-sdk-cpp/
- 检查日期：2026-10-30

## 环境与使用

- 准备支持 C++11 的编译器与 Make。

使用/检查入口（需先满足依赖条件）：

- `make`
- `make docs`

## 目录职责

- include/ — 游戏模型、通信与模拟器头文件
- example/ — control/simulate/template 示例
- Makefile — 编译与文档目标
- Doxyfile — API 文档配置

## 本次整理

- 新增维护文档和在线文档入口，补全用途、目录、使用路径及验证边界。
- 修复 Makefile 的头文件目录和依赖列表，从根目录改为 include/。

## 检查记录

- **仓库目录与入口盘点**（passed）：检查 Git 索引中的 16 个路径、README 和项目配置；不等于功能验收。
- **完整构建与端到端运行**（not_run）：3 个示例通过 MSVC /Zs /std:c++14 语法检查；未运行 Judger 比赛或模拟完整对局。
- **MSVC 示例语法检查**（passed）：cl /Zs /std:c++14 /EHsc /Iinclude 对 3 个 example/*.cpp 检查通过。

## 验证边界与待办

- 3 个示例通过 MSVC /Zs /std:c++14 语法检查；未运行 Judger 比赛或模拟完整对局。

## 后续维护约定

保留上游许可证与作者信息。沿用现有模块边界和格式配置；修复功能时同步最小回归验证。依赖或接口变更需写明迁移步骤，避免仅为目录美观搬动公开入口。
