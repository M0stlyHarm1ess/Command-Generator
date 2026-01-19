# Command Generator

一个完全通过html实现的的命令生成器项目，所有功能实现在一个单一的html中，无需环境依赖，快速启动。
用户只需要录入命令模板，通过点击更改变量，即可实现实时渲染，点击复制。



## 功能特点

- 📋 **命令管理**：创建、编辑、删除和排序命令模板
- 📁 **分栏组织**：按照分栏组织命令
- 🔍 **智能搜索**：支持通过命令标题、描述进行命令搜索
- 🏷️ **标签系统**：支持标签快速筛选相关命令
- 🎯 **变量管理**：使用`${{变量名}}`格式在命令中定义变量，支持动态替换，支持自动添加
- 📤 **数据导入导出**：支持JSON格式的数据备份和迁移，所有数据均保存在本地，无网络通信
- ⚡ **实时预览**：编辑变量时实时更新命令预览

## 界面展示


<img width="2882" height="1606" alt="image" src="https://github.com/user-attachments/assets/edd3381b-9279-4a61-88cf-93b7ce7becca" />
<img width="2877" height="1560" alt="image" src="https://github.com/user-attachments/assets/299f64fc-a3e2-40c4-aba7-a25eaa6012e7" />
<img width="2883" height="1576" alt="image" src="https://github.com/user-attachments/assets/072c6d4b-bee3-4de9-b59d-80f6f94bea1e" />



## 快速开始

### 直接使用

1. 克隆或下载项目文件
2. 直接在浏览器中打开 `command-generator.html` 文件
3. 开始使用命令生成器

### 本地服务器

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
- 所有命令点击即可复制
- 点击分栏菜单项可切换查看不同类型的命令
- 使用顶部搜索框可搜索命令
- 点击标签可筛选相关命令
- 点击排序按可拖动排序，自动保存

### 2. 编辑变量

- 右侧显示当前命令所需的变量
- 点击变量值可编辑，实时更新命令预览
- 变量值为空时，会显示占位符 `[变量名_PLACEHOLDER]`

### 3. 管理命令

- 点击「管理面板」进入命令管理界面
- 支持添加、编辑、删除命令
- 支持自动添加新变量
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

## 项目结构

```
command-generator.html  # 主应用文件
README.md               # 项目说明文档
```

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

## 许可证

MIT License

## 更新日志

### v0.2.0
- 初始版本发布
- 实现核心功能：命令管理、变量替换、分栏组织
- 支持搜索、标签筛选和拖放排序
- 包含默认示例数据
- 支持数据导入导出

