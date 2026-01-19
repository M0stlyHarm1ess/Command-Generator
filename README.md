# Command-Generator
# Command Generator

一个现代化的命令生成器，帮助您管理和生成各种系统和应用的命令模板。

## 功能特点

- 📋 **命令管理**：创建、编辑、删除和排序命令模板
- 📁 **分栏组织**：按系统或应用类型组织命令（Linux、Windows、SQL等）
- 🔍 **智能搜索**：支持命令标题、描述和模板的全文搜索
- 🏷️ **标签系统**：通过标签快速筛选相关命令
- 🎯 **变量替换**：使用`${{变量名}}`格式在命令中定义变量，支持动态替换
- 📱 **响应式设计**：适配不同屏幕尺寸
- 📤 **数据导入导出**：支持JSON格式的数据备份和迁移
- 🎨 **现代化UI**：简洁、专业的蓝灰色扁平设计
- ⚡ **实时预览**：编辑变量时实时更新命令预览

## 快速开始

### 直接使用

1. 克隆或下载项目文件
2. 直接在浏览器中打开 `command-generator2.html` 文件
3. 开始使用命令生成器

### 本地服务器（推荐）

```bash
# 使用Python启动本地服务器
python3 -m http.server 8888

# 或使用Node.js的http-server
npx http-server -p 8888

# 然后在浏览器中访问
http://localhost:8888/command-generator2.html
```

## 使用说明

### 1. 查看命令

- 左侧显示所有命令模板，按分栏组织
- 点击分栏菜单项可切换查看不同类型的命令
- 使用顶部搜索框可搜索命令
- 点击标签可筛选相关命令

### 2. 编辑变量

- 右侧显示当前命令所需的变量
- 点击变量值可编辑，实时更新命令预览
- 变量值为空时，会显示占位符 `[变量名_PLACEHOLDER]`

### 3. 管理命令

- 点击「管理面板」进入命令管理界面
- 支持添加、编辑、删除命令
- 支持为命令分配分栏和标签
- 支持拖放排序

### 4. 管理分栏

- 在管理面板的「分栏管理」中可添加、编辑、删除分栏
- 支持拖放排序分栏

### 5. 导入导出数据

- 在管理面板的「数据管理」中可导出当前数据为JSON文件
- 支持从JSON文件导入数据，可选择全新导入或增量导入

## 默认数据

首次打开时，系统会自动加载示例数据，包括：

### Linux系统操作
- Linux创建用户：`sudo useradd -m -s /bin/bash ${{USER_NAME}}`
- Linux文件权限：`chmod ${{PERMISSIONS}} ${{FILE_PATH}}`

### Windows系统操作
- Windows创建目录：`mkdir ${{DIR_PATH}}`
- Windows查看进程：`tasklist /fi "imagename eq ${{PROCESS_NAME}}.exe"`

### SQL操作
- SQL查询数据：`SELECT * FROM ${{TABLE_NAME}} WHERE ${{CONDITION}}`
- SQL插入数据：`INSERT INTO ${{TABLE_NAME}} (${{COLUMNS}}) VALUES (${{VALUES}})`

## 技术栈

- **前端框架**：原生HTML、CSS、JavaScript
- **样式设计**：CSS3变量、Flexbox布局、响应式设计
- **数据存储**：localStorage
- **图标**：纯CSS实现的图标
- **动画效果**：CSS3过渡和动画

## 项目结构

```
command-generator2.html  # 主应用文件
README.md               # 项目说明文档
```

## 浏览器兼容性

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 开发说明

### 代码组织

- **HTML结构**：清晰的语义化标签
- **CSS样式**：使用CSS变量统一管理颜色和样式
- **JavaScript逻辑**：模块化的函数设计

### 核心功能实现

- **变量提取**：使用正则表达式从命令模板中提取变量
- **命令筛选**：基于分栏、标签和搜索关键词的组合筛选
- **拖放排序**：HTML5 Drag and Drop API
- **实时更新**：事件驱动的UI更新机制

## 数据格式

### 命令数据

```json
{
  "title": "命令标题",
  "description": "命令描述",
  "tags": ["标签1", "标签2"],
  "template": "命令模板 ${{变量名}}",
  "columnId": "分栏ID",
  "sortOrder": 0
}
```

### 变量数据

```json
{
  "变量名1": "变量值1",
  "变量名2": "变量值2"
}
```

### 分栏数据

```json
[
  {
    "id": "column_id",
    "name": "分栏名称"
  }
]
```

## 贡献指南

欢迎提交Issue和Pull Request来帮助改进项目！

### 提交Pull Request

1. Fork本仓库
2. 创建特性分支：`git checkout -b feature/your-feature`
3. 提交更改：`git commit -m 'Add some feature'`
4. 推送到分支：`git push origin feature/your-feature`
5. 提交Pull Request

## 许可证

MIT License

## 更新日志

### v1.0.0
- 初始版本发布
- 实现核心功能：命令管理、变量替换、分栏组织
- 支持搜索、标签筛选和拖放排序
- 包含默认示例数据
- 支持数据导入导出

## 联系方式

如有问题或建议，欢迎通过GitHub Issues反馈。

---

**Command Generator** - 让命令管理更简单！ 🚀
