✨ 功能特性

📋 账号管理

· 账号申请：用户提交个人信息创建账号
· 信息查询：管理员查看所有用户信息（需密码）
· 自动编号：系统自动生成唯一账号ID

📝 帖子管理

· 发布帖子：认证用户可以发布交易帖子
· 回复帖子：对已有帖子进行回复交流
· 搜索功能：关键词搜索帖子和回复内容
· 编辑删除：修改或删除自己发布的内容

⚙️ 平台设置

· LOGO设置：自定义平台LOGO图片
· 背景设置：个性化平台背景图片
· 戳戳我页面：设置特殊展示图片

🔐 安全特性

· 本地存储：所有数据存储在浏览器中
· 密码验证：关键操作需要密码验证

🚀 快速开始

在线使用

1. 直接访问页面：index.html
2. 首次使用点击"申请账号"填写信息

本地运行

```bash
# 克隆或下载项目
git clone <repository-url>

# 无需安装依赖，直接打开
open index.html  # macOS
start index.html # Windows
xdg-open index.html # Linux
```

📁 项目结构

```
原味交易平台/
├── index.html          # 主页面文件
├── README.md           # 项目说明文档
└── 代码说明/           # 详细代码文档
```

🔧 技术栈

· 前端：HTML5, CSS3, JavaScript (ES6+)
· 存储：LocalStorage (浏览器本地存储)
· UI组件：Font Awesome图标库
· 响应式：移动优先的响应式设计

📊 数据模型

账号信息

```javascript
{
  id: "ACC20231215001",
  nickname: "用户昵称",
  username: "用户名称",
  phoneTail: "1234",
  age: 25,
  height: 175,
  weight: 65,
  attribute: "1",
  smAttribute: "S",
  dickLength: 18.5,
  dickThickness: 4.2,
  specialPreferences: "原味/圣水",
  date: "2023-12-15 10:30:00"
}
```

帖子信息

```javascript
{
  id: "20231215001",
  nickname: "发帖人",
  phoneTail: "5678",
  title: "交易标题",
  tradeTypes: ["袜子", "内裤"],
  targetGroups: ["军", "警"],
  tradeMethod: "快递",
  price: 200,
  requirements: "具体要求说明",
  date: "2023-12-15 10:30:00"
}
```

💻 使用说明

用户流程

1. 申请账号 → 填写个人信息 → 获取用户密码
2. 发布帖子 → 输入用户密码 → 填写帖子内容
3. 回复帖子 → 输入用户密码 → 填写回复内容

管理员流程

1. 查看所有信息 → 输入管理员密码 → 查看全部数据
2. 平台设置 → 输入管理员密码 → 上传图片/修改设置

🌐 浏览器兼容性

浏览器 支持情况 备注
Chrome 80+ ✅ 完全支持 推荐使用
Firefox 75+ ✅ 完全支持 
Edge 80+ ✅ 完全支持 
Safari 13+ ✅ 基本支持 
移动浏览器 ✅ 响应式支持 适配移动端

⚠️ 注意事项

1. 数据安全：
   · 所有数据存储在浏览器本地
   · 清除浏览器数据会导致数据丢失
   · 建议定期备份重要数据
2. 密码管理：
   · 密码为硬编码，实际使用中建议定期更改
   · 不要在生产环境使用默认密码
3. 图片上传：
   · 支持JPG、JPEG、PNG格式
   · 建议LOGO尺寸：75×75像素
   · 图片以Base64格式存储

🔄 版本历史

v1.0.0 (当前版本)

· ✅ 账号申请和管理功能
· ✅ 帖子发布和回复系统
· ✅ 平台设置（LOGO、背景、图片）
· ✅ 本地数据存储
· ✅ 响应式设计
· ✅ 密码保护系统

📱 响应式设计

平台采用移动优先的设计理念：

· 桌面端：多列布局，完整功能展示
· 平板端：适配中等屏幕
· 手机端：单列布局，触控优化

🔍 功能截图

主页界面

```
[账号信息] [信息查询] [发布帖子] [回复帖子] [设置] [戳戳我]
```

发布帖子界面

· 自动生成帖子编号
· 多种交易类型选择
· 定向人群筛选
· 价格和详细要求

🛠️ 开发说明

本地开发

1. 使用任何现代代码编辑器打开项目
2. 修改代码后直接刷新浏览器查看效果
3. 所有数据存储在localStorage中

数据备份

```javascript
// 备份数据
const backupData = {
  accounts: JSON.parse(localStorage.getItem('accountData')),
  posts: JSON.parse(localStorage.getItem('postData')),
  replies: JSON.parse(localStorage.getItem('replyData'))
};

// 恢复数据
localStorage.setItem('accountData', JSON.stringify(backupData.accounts));
```

🤝 贡献指南

欢迎提交Issue和Pull Request：

1. Fork 项目
2. 创建功能分支
3. 提交更改
4. 发起Pull Request

📄 许可证

本项目仅供学习和研究使用，请遵守相关法律法规。

❓ 常见问题

Q: 数据会丢失吗？

A: 数据存储在浏览器本地，清除浏览器缓存会丢失数据。

Q: 如何更改密码？

A: 在代码中修改DEFAULT_USER_PASSWORD和DEFAULT_ADMIN_PASSWORD变量。

Q: 支持导出数据吗？

A: 目前不支持直接导出，但可以通过浏览器开发者工具访问localStorage。

Q: 能多人同时使用吗？

A: 每个浏览器实例独立，数据不共享。

---

注意：本项目为纯前端实现，适合个人使用或小范围场景。如有大规模使用需求，建议开发后端支持。
