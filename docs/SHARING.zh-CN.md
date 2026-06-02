# 对外分享指南

> 语言：中文 | English: [`SHARING.md`](SHARING.md)

## 无需 NDA 可分享内容
当前建议分享的公开材料：
- [README](../README.zh-CN.md)
- [当前公开状态](STATUS_UPDATE_2026-05-30.zh-CN.md)
- [公开披露范围](PUBLIC_SCOPE.zh-CN.md)
- [路线图](ROADMAP.zh-CN.md)

日期为 2026-02-10 的 v0.9 非保密技术包现在是已取代的历史包。不要把它作为项目当前技术包继续分享。

## 禁止分享
- `docs/_confidential_DO_NOT_SHARE/`
- 任何 `references/` 内容
- 任何 PDF、截图或提取的图表

## 快速打包（Windows PowerShell）
如需为审计目的打包历史材料，请在文件名和说明中明确标记 historical/superseded，并包含当前状态更新：

```powershell
$root = Resolve-Path .
$src = Join-Path $root "docs\nonconfidential"
$dst = Join-Path $root "Eco-Cat-Food_Public_Status_And_Historical_Package.zip"
if (Test-Path $dst) { Remove-Item $dst -Force }
$paths = @(
  Join-Path $root "README.zh-CN.md",
  Join-Path $root "docs\STATUS_UPDATE_2026-05-30.zh-CN.md",
  Join-Path $root "docs\PUBLIC_SCOPE.zh-CN.md",
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
仅在明确的审计或历史复盘场景下使用历史材料。历史非保密包状态与排除范围说明见[历史非保密包索引](nonconfidential/00-PACKAGE_INDEX.NC.zh-CN.md)（或[英文版](nonconfidential/00-PACKAGE_INDEX.NC.md)）。
