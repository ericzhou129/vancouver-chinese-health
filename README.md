# 温哥华华人医疗互助网站 (Vancouver Chinese Healthcare Community)

## 🚀 新功能说明

### 1. 社交媒体分享预览
现在当你分享文章链接到社交媒体时，会显示漂亮的预览卡片，包括：
- 文章标题
- 文章描述
- 预览图片
- 网站名称

**使用方法：**
- 分享主页：`https://anxinhealth.vercel.app`
- 分享具体文章：`https://anxinhealth.vercel.app/healthcare-guide` 或 `https://anxinhealth.vercel.app/msp-insurance-guide`

### 2. 内容管理系统
访问 `/admin.html` 可以使用简单的管理界面来：
- 创建新文章
- 管理现有文章
- 更新微信群二维码
- 修改网站设置

### 3. 兼容性设计
- **保持原有链接有效**：所有 `#healthcare-guide` 格式的链接仍然可以正常访问
- **新的分享友好链接**：`/healthcare-guide` 格式的链接在分享时会显示正确的预览

## 📁 文件结构

```
vancouver-chinese-health/
├── index.html                    # 主页面（包含所有文章内容）
├── healthcare-guide.html         # 医疗指南文章的分享页面
├── msp-insurance-guide.html      # MSP指南文章的分享页面
├── admin.html                    # 管理后台
├── wechat-qr-code.jpg           # 微信群二维码
├── data/
│   └── articles.json            # 文章元数据
├── assets/
│   └── images/
│       ├── create-og-images.html # 生成社交媒体预览图的工具
│       ├── healthcare-guide-og.jpg
│       ├── msp-guide-og.jpg
│       └── site-og-default.jpg
└── package.json                 # 项目配置文件
```

## 🛠️ 如何更新内容

### 更新现有文章
1. 直接编辑 `index.html` 中的文章内容
2. 如果修改了标题或描述，同时更新：
   - 对应的 `.html` 文件（如 `healthcare-guide.html`）
   - `data/articles.json` 中的元数据

### 添加新文章
1. 访问 `/admin.html`
2. 在"文章管理"标签页填写文章信息
3. 点击"生成文章页面"
4. 将生成的HTML保存为 `[article-id].html`
5. 在 `index.html` 中添加文章内容
6. 更新 `data/articles.json`

### 更新微信二维码
1. 访问 `/admin.html`
2. 切换到"二维码管理"标签页
3. 上传新的二维码图片
4. 将新图片保存为 `wechat-qr-code.jpg`
5. 替换仓库中的原文件

## 🎨 创建社交媒体预览图

1. 在浏览器中打开 `/assets/images/create-og-images.html`
2. 点击相应按钮生成预览图
3. 保存生成的图片到 `/assets/images/` 目录

## 📋 检查清单

部署前请确认：
- [ ] 所有文章的 `.html` 文件都已创建
- [ ] `data/articles.json` 包含所有文章的元数据
- [ ] 社交媒体预览图片都已上传
- [ ] 微信二维码是最新的
- [ ] 在本地测试过所有链接

## 🔗 重要链接

- 网站首页：https://anxinhealth.vercel.app
- 医疗指南：https://anxinhealth.vercel.app/healthcare-guide
- MSP指南：https://anxinhealth.vercel.app/msp-insurance-guide
- 管理后台：https://anxinhealth.vercel.app/admin.html

## 💡 提示

1. **测试社交媒体预览**：
   - Facebook: https://developers.facebook.com/tools/debug/
   - Twitter: https://cards-dev.twitter.com/validator
   - LinkedIn: https://www.linkedin.com/post-inspector/

2. **SEO优化**：
   - 每篇文章都有独立的URL，有利于搜索引擎收录
   - 使用结构化的元数据提高搜索排名

3. **性能优化**：
   - 图片已优化为合适的尺寸（1200x630px）
   - 使用静态HTML确保快速加载

## 📞 需要帮助？

如有问题，请查看管理后台的操作说明，或联系技术支持。