# LogLens

在本地把杂乱的 JSON 日志转换成可搜索、可筛选的开发者报告，不上传任何数据。

## 适合谁

- 需要快速定位接口错误的后端开发者
- 希望在提交 Bug 前整理日志的测试人员
- 不方便把生产日志上传到在线工具的团队

## 快速开始

```bash
npm install
node index.js ./examples/app.log --level error
```

运行后将在当前目录生成 `report.html`。用浏览器打开即可按时间、级别和关键词筛选。

## 常用命令

```bash
# 只查看错误日志
node index.js app.log --level error

# 指定输出文件
node index.js app.log --output incident-report.html
```

## 常见问题

**日志会上传吗？**  
不会。解析和报告生成均在本机完成。

**支持哪些格式？**  
默认支持每行一个 JSON 对象的日志文件；其他格式可通过解析器扩展。

