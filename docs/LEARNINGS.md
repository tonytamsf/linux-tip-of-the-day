# Project Learnings

This file documents useful information, discoveries, and key insights about the project.

## Git LFS Setup (2025-12-27)

### Overview
Git LFS (Large File Storage) has been configured to handle large media files efficiently. Instead of storing large files directly in Git, LFS stores them on a separate server and replaces them with small pointer files in the repository.

### Configured File Types
The following file types are automatically tracked by Git LFS:
- Video files: `*.mov`, `*.mp4`, `*.mkv`, `*.avi`
- Audio files: `*.wav`, `*.flac`
- Design files: `*.psd`
- Archives: `*.zip`

Configuration is stored in `.gitattributes` file.

### Files Currently Tracked
The following media files have been added to the repository with LFS:
- `days/day1/inux day 1.mov` (61MB)
- `days/day1/video1790997722.mp4` (7.7MB)
- `days/day2/LINUX DAY 2.mov` (121MB)
- `days/day2/Linux day 2 raw.mp4` (53MB)

### How to Use Git LFS
1. **Installation**: Git LFS is installed via Homebrew (`/opt/homebrew/bin/git-lfs`)
2. **Cloning**: When you clone or pull, files are automatically downloaded
3. **Adding new media files**: Simply `git add` files matching the LFS patterns - they'll automatically be tracked by LFS
4. **Checking LFS status**: Use `git lfs ls-files` to see all LFS-tracked files

### Important Notes
- The repository contains 2 commits related to LFS setup (be371ca and 36b93f1)
- When pushing/pulling, you need proper authentication to the GitHub repository
- Large file downloads may take longer on first clone/pull, but subsequent operations are faster
