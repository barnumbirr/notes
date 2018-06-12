# Git

## Squash all commits into one

Make sure everything is committed, and write down the latest ```commit_id``` in case something goes wrong, or create a separate branch as a backup.

Reset your head to the first commit, but leave your index unchanged. All changes since the first commit will now appear ready to be committed.

```bash
git reset --soft `git rev-list --max-parents=0 --abbrev-commit HEAD`
```

Amend your commit to the first commit and change the commit message.

```bash
git commit --amend -m "initial commit"

# if you want to keep the existing commit message
git commit --amend --no-edit
```

Force push your changes.

```bash
git push -f
```

<p style="font-size: 10px" align="right">
    from <a href="https://stackoverflow.com/a/49900667">Stackoverflow</a>
</p>

