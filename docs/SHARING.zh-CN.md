# 对外分享指南

> 语言：中文 | English: [`SHARING.md`](SHARING.md)

## 无需 NDA 可分享内容
最简单：
- 发送单文件（英文，默认）：`docs/nonconfidential/Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.en-US.md`
- 可选附上中文版本：`docs/nonconfidential/Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.zh-CN.md`

或（如果你更喜欢文件夹/zip）：
- 仅分享：`docs/nonconfidential/`（请排除任何 `archive/` 本地草稿）

## 禁止分享
- `docs/_confidential_DO_NOT_SHARE/`
- 任何 `references/` 内容
- 任何 PDF、截图或提取的图表

## 快速打包（Windows PowerShell）
创建只包含“可分享文件”的 zip（排除本地草稿目录）：

```powershell
$root = Resolve-Path .
$src = Join-Path $root "docs\nonconfidential"
$dst = Join-Path $root "Eco-Cat-Food_NonConfidential_Package.zip"
if (Test-Path $dst) { Remove-Item $dst -Force }
$paths = @(
  Join-Path $src "00-PACKAGE_INDEX.NC.md",
  Join-Path $src "00-PACKAGE_INDEX.NC.zh-CN.md",
  Join-Path $src "04-References.NC.tsv",
  Join-Path $src "04-References.NC.csv",
  Join-Path $src "05-DOI-Verification.NC.tsv",
  Join-Path $src "05-DOI-Verification.NC.csv",
  Join-Path $src "Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.en-US.md",
  Join-Path $src "Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.zh-CN.md"
)
Compress-Archive -Path $paths -DestinationPath $dst
```

## 备注
非保密技术包的包含/排除范围说明见 `docs/nonconfidential/00-PACKAGE_INDEX.NC.zh-CN.md`（或英文版 `00-PACKAGE_INDEX.NC.md`）。
