# House Builder Pattern

基于 **生成器模式（Builder Pattern）** 的房屋信息生成系统：用同一套构建流程产出经济型、普通型、豪华型三种房屋配置，配合 Swing 图形界面交互式配置各功能区。

## 技术栈

Java · Swing · Eclipse · 生成器模式 / 工厂模式 / 观察者模式

## 模块划分

| 模块 | 类 | 职责 |
| --- | --- | --- |
| 产品模型 | `House` | 房屋对象：面积、卧室 / 浴室 / 车库 / 花园 / 泳池 |
| 抽象构建器 | `HouseBuilder` | 定义建造步骤，内含 6 个功能区监听器 |
| 具体构建器 | `EconHouseBuilder`、`NormHouseBuilder`、`LuxHouseBuilder` | 经济型 / 普通型 / 豪华型 |
| 指挥者 | `Director` | 封装构建顺序 |
| 图形界面 | `HouseBuyerGUI` | Swing 界面 + `BuilderFactory` 选择构建器 |

## 规模

源文件 7 个 · 代码 859 行 · 类 15 个 · 设计模式 3 种

## 运行

```bash
javac *.java
java HouseBuyerGUI
