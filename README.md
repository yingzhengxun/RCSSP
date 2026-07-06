This mod can keep your server well-organized!
# 中文版
# 服务器登录插件

一个基于 Fabric 框架的 Minecraft 服务器端登录插件，提供完整的注册/登录系统、积分机制和传送功能。

## 功能特性

### 🔐 登录系统
- **`/register <用户名> <密码>`** - 注册新账号，自动获得 100 初始积分
- **`/login <用户名> <密码>`** - 使用已注册账号登录
- 未登录玩家无法移动和发送聊天消息
- 密码使用 SHA-256 加密存储，安全可靠

### 💰 积分系统
- 新注册用户自动获得 **100 积分**
- 传送命令每次消耗 **10 积分**（OP 玩家免费）
- **`/givecredit <用户名> <数量>`** - OP 专属指令，可给予玩家积分（上限 100000）

### 🚀 传送功能

#### TPA 传送
- **`/tpa <玩家名>`** - 向目标玩家发送传送请求
- **`/tpaccept`** - 接受传送请求
- **`/tpdeny`** - 拒绝传送请求

#### 家园系统
- **`/sethome <名称>`** - 设置家园位置（最多 5 个）
- **`/home <名称>`** - 传送到指定家园
- **`/homes`** - 查看所有家园列表
- **`/delhome <名称>`** - 删除家园

#### 公共传送点
- **`/setwarp <名称>`** - OP 专属，设置公共传送点（最多 5 个）
- **`/warp <名称>`** - 传送到指定传送点
- **`/warps`** - 查看所有传送点列表
- **`/delwarp <名称>`** - OP 专属，删除传送点

#### 返回功能
- **`/back`** - 返回上一次传送前的位置

## 技术细节

| 属性 | 值 |
|------|-----|
| **Mod ID** | `yrc-login` |
| **适用游戏版本** | Minecraft 1.20.1 |
| **加载环境** | 仅服务端（Server） |
| **依赖** | Fabric API, Java 17+ |

## 安装方法

1. 确保你的服务器已安装 **Fabric Loader 0.19.3+**
2. 安装 **Fabric API**
3. 将 `yrc-login-XXX.jar` 放入服务器的 `mods` 目录
4. 启动服务器，插件会自动生成数据目录
5. **注意⚠️：从1.2.2alpha-2开始，客户端必须安装此mod,并且该版本以下的mod均为实验品，可能防不住毁图者**
6. **警告⚠️：若您尝试在forge上使用信雅互联模组加载此mod，通常会报出“Internal Exception”类的错误，这是因为forge+信雅互联对线程安全、事件触发时机做了严格限制；当报出此错误时，您应当反馈到forge或者信雅互联的社区，而非在本mod的github仓库提交issues。**

## 数据存储

玩家数据（账号、积分、家园位置等）以 JSON 格式存储在服务器目录中，数据持久化保存。

## 权限说明

- **普通玩家**：可使用 `/register`、`/login`、传送命令（需消耗积分）
- **OP 玩家**：拥有无限积分，可使用 `/givecredit`、`/setwarp`、`/delwarp` 指令
# For English
# YRC Login Mod

A Fabric-based Minecraft server-side login plugin providing a complete registration/login system, credit mechanism, and teleportation features.

## Features

### 🔐 Login System
- **`/register <username> <password>`** - Register a new account, automatically receive 100 initial credits
- **`/login <username> <password>`** - Login with registered account
- Unlogged players cannot move or send chat messages
- Passwords are encrypted using SHA-256 for secure storage

### 💰 Credit System
- New users automatically receive **100 credits** upon registration
- Teleport commands cost **10 credits** each (OP players are free)
- **`/givecredit <username> <amount>`** - OP-only command to give credits to players (max 100000)

### 🚀 Teleportation Features

#### TPA Teleport
- **`/tpa <playername>`** - Send a teleport request to target player
- **`/tpaccept`** - Accept incoming teleport request
- **`/tpdeny`** - Deny incoming teleport request

#### Home System
- **`/sethome <name>`** - Set a home location (max 5 homes)
- **`/home <name>`** - Teleport to specified home
- **`/homes`** - View all homes list
- **`/delhome <name>`** - Delete a home

#### Public Warps
- **`/setwarp <name>`** - OP-only, set a public warp point (max 5 warps)
- **`/warp <name>`** - Teleport to specified warp
- **`/warps`** - View all warps list
- **`/delwarp <name>`** - OP-only, delete a warp

#### Back Function
- **`/back`** - Return to the previous location before last teleport

## Technical Details

| Property | Value |
|----------|-------|
| **Mod ID** | `yrc-login` |
| **Game Version** | Minecraft 1.20.1 |
| **Environment** | Server-side only |
| **Dependencies** | Fabric API, Java 17+ |

## Installation

1. Ensure your server has **Fabric Loader 0.19.3+** installed
2. Install **Fabric API**
3. Place `yrc-login-XXX.jar` into the server's `mods` directory
4. Start the server, the plugin will automatically generate data directory
5. **⚠️ Notice: Starting from version 1.2.2alpha-2, this mod is mandatory for all clients. All mod versions prior to this release are experimental builds and may fail to protect against map griefers.**
6. **Warning ⚠️: If you attempt to load this mod on Forge with the Sinytra Connector mod, errors categorized as "Internal Exception" will usually occur. This happens because Forge paired with Sinytra Connector enforces strict restrictions on thread safety and event trigger timings. When you encounter this error, please submit feedback to the Forge or Sinytra Connector communities instead of filing issues in this mod's GitHub repository.**

## Data Storage

Player data (accounts, credits, home locations, etc.) is stored in JSON format in the server directory, with persistent data preservation.

## Permissions

- **Regular Players**: Can use `/register`, `/login`, and teleport commands (credits required)
- **OP Players**: Have unlimited credits, can use `/givecredit`, `/setwarp`, `/delwarp` commands
