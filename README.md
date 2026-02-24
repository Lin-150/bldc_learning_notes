# BLDC 控制算法学习笔记

> 仓库用途：记录 BLDC（无刷直流电机）控制算法的学习过程、代码实现、调试经验和知识点总结
> 开发环境：Cursor / VS Code + 嵌入式开发工具链（如STM32CubeIDE、PlatformIO）

## 📚 学习目录
| 章节 | 核心内容 | 状态 |
|------|----------|------|
| 01 | BLDC 基本原理（结构、换相、霍尔传感器） | ✅ 已完成 |
| 02 | 六步换相控制算法（硬件驱动、时序逻辑） | 🚧 进行中 |
| 03 | FOC 磁场定向控制（Clark/Park变换、SVPWM） | 📋 待学习 |
| 04 | 速度闭环控制（PI调节器、编码器/霍尔测速） | 📋 待学习 |
| 05 | 硬件适配（STM32/ESP32 驱动电路） | 🚧 进行中 |

## 🔧 开发环境
- **主控芯片**：STM32F103C8T6 / ESP32 / CMS32M6736EQFN48 / FU6572N / LKS32MC03x（可替换为你使用的芯片）
- **编译工具链**：ARM GCC / ESP-IDF / keil
- **调试工具**：OpenOCD + GDB / 串口调试助手
- **依赖库**：STM32HAL库 / Arduino Core for ESP32 / 中微电机库 / 峰迢电机库 / 凌鸥创芯电机库

## 📝 核心代码说明
| 文件/目录 | 功能说明 |
|-----------|----------|
| `src/6step_commutation/` | 六步换相控制核心代码（GPIO驱动、霍尔中断、换相逻辑） |
| `src/foc/` | FOC控制算法（Clark/Park变换、SVPWM实现） |
| `src/utils/` | 通用工具函数（PI调节器、滤波算法、串口打印） |
| `docs/` | 学习笔记、公式推导、硬件原理图 |
| `examples/` | 可直接运行的示例代码（适配具体开发板） |

## 🚀 快速上手
### 1. 克隆仓库
```bash
git clone https://github.com/Lin-150/bldc_learning_notes.git
cd bldc_learning_notes
