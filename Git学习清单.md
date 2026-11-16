# Git → GitHub 协作学习清单

> 学法：每一步自己敲命令，可可检查结果。练习仓库：本文件夹（已推到 tangyuqi666/sound-sim-training）。

- [x] 1. 本地仓库起步：init / status / add / commit / log（11-15）
- [x] 2. 看清改动：diff / diff --staged / show，.gitignore 忽略规则（11-15）
- [x] 3. 后悔药：restore / commit --amend / revert（11-15）
- [x] 4. 分支：switch -c / merge / 亲手解一次冲突（11-15）
- [x] 5. 连上 GitHub：SSH key / remote / push -u（11-15）
- [x] 6. 协作主流程：分支 → push → PR → review → merge（11-15）
- [x] 7. 同步别人的改动：pull --ff-only / rebase / 推送被拒（11-15）
- [ ] 8. 给别人的项目提 PR：fork → clone → 改 → push → PR 到上游
- [ ] 9. 选修：stash / cherry-pick / tag / 交互式 rebase

## 踩过的坑（都是真踩的）

- 解冲突时只删了 `<<<<<<<` `=======` `>>>>>>>` 三行，把 `HEAD` 和 `feature/plan` 两个名字留在文件里 → 已修（b026118）
- `--am` 写了两个横杠，git 当成长选项，报 pathspec 找不到文件；短选项是一个横杠 `-am`
- rebase 卡在冲突时没 `git add` 就 `commit -am`，把自己那一版丢了；靠 `git reflog` 找回（e4e4ffe），再补一次提交
- 新建远端仓库时勾了 README 会让两边历史互不相干，push 直接被拒；空仓库才对

## 进度日志

- 11-15 11:14 首次提交 c59c702
- 11-15 12:10 .gitignore 提交 f43828d
- 11-15 17:02 五条历史（含 revert 与 reapply）
- 11-15 17:39 分支合并 9321f6a，冲突已解
- 11-15 18:24 SSH 通（tangyuqi666），main 推上远端
- 11-15 20:31 PR #1 合并（1d53ce4）
- 11-15 21:56 rebase 丢改动已补回，HEAD c29fcd4，本地与远端一致
