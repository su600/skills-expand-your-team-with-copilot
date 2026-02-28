# Mergington 高中课外活动

一个简单的网页应用，允许学生查看并报名参加课外活动。

## 功能

- 查看所有可用的课外活动
- 报名参加活动

## 开发指南

详细的环境搭建与开发说明，请参阅 [开发指南（英文）](docs/how-to-develop.md)。

## 快速开始

### 安装依赖

```bash
pip install -r src/requirements.txt
```

### 运行应用

```bash
python -m uvicorn src.app:app --host 0.0.0.0 --port 8000
```

打开浏览器，访问：
- 应用首页：http://localhost:8000
- API 文档：http://localhost:8000/docs

## API 接口

| 方法 | 路径                                                              | 说明                       |
| ---- | ----------------------------------------------------------------- | -------------------------- |
| GET  | `/activities`                                                     | 获取所有活动及当前报名人数 |
| POST | `/activities/{activity_name}/signup?email=student@mergington.edu` | 报名参加某项活动           |

> [!IMPORTANT]
> 所有数据保存在内存中，服务器重启后数据将会重置。

---

&copy; 2025 GitHub &bull; [行为准则](https://www.contributor-covenant.org/zh-cn/version/2/1/code_of_conduct/) &bull; [MIT 许可证](https://gh.io/mit)
