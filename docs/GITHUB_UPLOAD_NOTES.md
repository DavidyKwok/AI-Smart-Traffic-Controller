# GitHub Upload Notes

This folder is prepared for GitHub.

Recommended upload steps:

```bash
git init
git add .
git commit -m "Initial commit: AI smart traffic light controller"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/AI-Smart-Traffic-Light-Controller.git
git push -u origin main
```

Before pushing, check file sizes:

```powershell
Get-ChildItem -Recurse -File |
Sort-Object Length -Descending |
Select-Object -First 30 FullName, @{Name="SizeMB";Expression={[math]::Round($_.Length / 1MB, 2)}}
```

Do not commit generated runtime folders after running the controller. The `.gitignore` file is set up to ignore the main output folders, video files, Python cache files, and temporary training artifacts.

The full project report PDF was not included because it contains academic/personal information. Selected figures were extracted into `assets/report_figures/` for the README.
