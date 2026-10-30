# Costume Gallery 服装参考库

衣装参考资产库（COSTUME-DB-01，原名「衣装集」），来自 <https://ai-costume-gallery.pages.dev/> 的本地镜像。

相关图库：
- 线稿姿态图：<https://ai-pose-gallery.pages.dev/>
- 深度姿态图：<https://ai-pose-depth-gallery.pages.dev/>

## 资产概览

- **总图片量**: 1407 张 PNG 原图（原寸）
- **分类（按季节/场景）**: 春 215、夏 254、秋 244、冬 253、内衣 199、派对 48、泳装 54、性感 140
- **内容**: 人物不入镜，仅衣装本体（face / 体型 / 背景需另行指定）
- **目录结构**: `分类/ID.png`（如 `春/SPR-0001.png`）

## 元数据

[`metadata_index.json`](./metadata_index.json) 每项字段：

- `id`: 全局唯一编号（`SPR` 春 / `SUM` 夏 / `AUT` 秋 / `WIN` 冬 / `LNG` 内衣 / `PTY` 派对 / `SWM` 泳装 / `SXY` 性感）
- `category`: 分类
- `keywords`: 衣装关键词（英文：色 / 单品 / 配饰）
- `local_path`: 本地相对路径（分类目录已由日语改中文）
- `local_path_original_ja`: 原始日文路径，便于回溯
- `original_url`: 原寸 PNG 地址（已下载）
- `webp_url` / `thumb_url`: WebP 预览与缩略图地址（未下载，可另行获取）
- `meta.total` / `meta.counts`: 总量与分类统计

## 重新同步

```bash
curl -sL https://ai-costume-gallery.pages.dev/index.json    # 元数据（不含图片地址）
# 图片地址内嵌在首页 HTML 的 `const D=[...]` 中：thumb=thumbs/ID.webp、webp=img/ID.webp、原寸=png/ID.png
```

## 日语 → 中文 对照

| 原文 | 中文 |
|---|---|
| 春 / 夏 / 秋 / 冬 | 春 / 夏 / 秋 / 冬（汉字同形） |
| ランジェリー | 内衣 |
| パーティ | 派对 |
| 水着 | 泳装 |
| セクシー | 性感 |
| 衣装集 | 服装集 |
| 原寸 | 原图（原尺寸） |
| サムネ | 缩略图 |
| キーワード | 关键词 |
| カテゴリ | 分类 |
