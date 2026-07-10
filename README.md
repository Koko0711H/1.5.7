# 深柴新产品 3D 展示站

这是基于原「深柴1.5.2」项目创建的独立新产品版本。它保留了原项目的滚动驱动 3D 镜头、模块导航、双语切换和科技感视觉效果。

## 快速开始

```bash
pnpm install
pnpm dev
```

生产构建：

```bash
pnpm build
```

## 修改产品内容

优先编辑 `src/productConfig.js`：

- `copy`：中英文产品文案、模块标题和导航文案
- `stages`：各模块的镜头位置、视角和旋转角度
- `stats`：右侧技术参数标签
- `footer`：页脚信息
- `modelUrl`：替换 3D 模型文件路径

当前副本使用 `public/generator.glb`，模型已做 Draco 几何压缩并压缩纹理，文件约 4.88MB，适合 Cloudflare 部署；`public/draco/` 内保留了解码器。其余文案、图片、标题、布局和交互均保持原网页版本。

Cloudflare Pages 拖拽部署时，直接拖拽 `cloudflare-upload` 文件夹中的全部内容；也可以拖拽 `dist` 文件夹中的全部内容。
