# UE Material Library

A reusable Unreal Engine material library with master materials, material instances,
material functions, parameter collections, fonts, foliage presets, and texture assets.

这是一个可复用的 Unreal Engine 材质资源库，包含母材质、材质实例、材质函数、参数集、字体材质、植被预设和贴图资源。

> Note: the repository name is currently `UE-Material_Libray`. If you rename it later, `UE-Material_Library` is the corrected spelling.

## Repository Snapshot

This snapshot contains 1,101 tracked files. Most of the repository is Unreal Engine
binary content, so Git LFS is required before using the assets in a real project.

当前仓库主要由 Unreal Engine 二进制资源组成，使用前请先安装并拉取 Git LFS 文件。

## Content Map

| Path | Count | Purpose |
| --- | ---: | --- |
| `Content/Texture` | 721 | Texture maps, including scene textures and location textures |
| `Content/Material_Instance` | 157 | Ready-to-use material instances |
| `Content/MaterialPlant` | 99 | Foliage and Megascans-style material presets |
| `Content/Material_Master` | 73 | Master materials and shared material bases |
| `Content/Material_Functions` | 36 | Reusable material functions |
| `Content/MaterialFont` | 6 | Font-related material assets |
| `Content/MaterialParameter` | 5 | Material parameter collections and shared controls |

## Recommended Setup

1. Install Git LFS:

```powershell
git lfs install
```

2. Clone the repository:

```powershell
git clone https://github.com/JHJ124/UE-Material_Libray.git
```

3. Pull the real asset files:

```powershell
cd UE-Material_Libray
git lfs pull
```

4. Copy or migrate the `Content` folder into your Unreal Engine project.

5. Open the project in Unreal Engine and run `Fix Up Redirectors` on the imported folders.

## Naming Guide

| Prefix | Meaning |
| --- | --- |
| `M_` | Master material |
| `MI_` | Material instance |
| `MF_` | Material function |
| `MPC_` / `MP_` | Material parameter collection or shared material parameter asset |
| `T_` | Texture |
| `BP_` | Blueprint helper asset |

## Git LFS Notes

Unreal assets are stored through Git LFS. If a `.uasset` file is only around 100-150
bytes, it is probably an LFS pointer file instead of the real asset. Run:

```powershell
git lfs pull
```

The LFS rules currently cover Unreal binary asset types such as `.uasset`, `.umap`,
`.ubulk`, `.uexp`, `.locres`, and `.locmeta`.

## Troubleshooting

- If materials appear pink or missing, make sure all LFS files were pulled successfully.
- If textures are missing after moving folders, use Unreal Engine's `Fix Up Redirectors`.
- If the repository is slow to clone, clone first with `GIT_LFS_SKIP_SMUDGE=1`, then run `git lfs pull` when you are ready to download the large files.

## 中文说明

这个仓库适合用作 UE 项目的材质资源库。推荐流程是先用 Git LFS 完整拉取资源，再把 `Content` 目录迁移到你的 Unreal Engine 项目中。

主要结构：

- `Material_Master`：母材质和通用材质基础。
- `Material_Instance`：可直接使用或二次调整的材质实例。
- `Material_Functions`：可复用材质函数。
- `Texture`：材质对应的贴图资源。
- `MaterialParameter`：全局参数和共享控制。
- `MaterialPlant`：植被相关材质预设。
