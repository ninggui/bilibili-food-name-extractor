<img src="./assets/cover.svg" alt="B站探店店名提取：从视频到收藏夹，中间到底错了几次？" width="100%">

# 本仓库已合并归档

> **本仓库内容已合并至 [bilibili-food-map-skill](https://github.com/ninggui/bilibili-food-map-skill)，请前往新地址查看与使用。**

## 为什么合并

本仓库（`bilibili-food-name-extractor`）与 [bilibili-food-map-skill](https://github.com/ninggui/bilibili-food-map-skill) 内容重复——两者主题一致（B站探店UP主视频 → 店名自动提取 → 七项校准 → 结构化文档）。

`bilibili-food-map-skill` 是完整可执行版本，包含：
- `SKILL.md` 主入口与执行规则
- 更详细的 7 项校验标准、质量门禁、反爬细则
- 已验证城市数据、断点续传状态板、12 个实战坑

本仓库的方法论精华（三种提取方式、与下游仓库的关系、适用边界、脱敏说明、实测数据）已全部并入 `bilibili-food-map-skill`。

## 上下游关系（保留说明）

```
B站视频 → [bilibili-food-map-skill] 提取+校准店名 → 结构化文档
                                        ↓
            [map-favorites-migration] 批量写入地图收藏夹
                                        ↓
                              手机导航直接用
```

- 上游：[bilibili-food-map-skill](https://github.com/ninggui/bilibili-food-map-skill)（B站视频 → 店名提取 → 校准 → 文档）
- 下游：[map-favorites-migration](https://github.com/ninggui/map-favorites-migration)（地图收藏迁移与坐标偏移修复）

## 脱敏说明

原方法论文档发布前做过以下处理：
- 不包含任何真实UP主ID、UID、粉丝数
- 不包含任何真实店名、地址、经纬度
- 不包含任何账号信息、会话凭据
- 涉及具体数量只保留量级（如"约1200家""90-95%"），不保留可定位到个体的信息
