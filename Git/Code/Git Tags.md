# Git Tags

Information about Git Tags, how to create/delete etc.

---

## Create Tags

To create a tag (lightweight):

```bash
git tag TAGNAME
```

To create a tag (annotated):

```bash
git tag -a TAGNAME -m "TAG_COMMIT_MESSAGE"
```

## Delete Tags

Delete a local tag:

```bash
git tag -d TAGNAME
```

Delete a remote tag:

```bash
git push --delete origin TAGNAME
```

Delete local tags that don't exist on remote:

```bash
git fetch origin refs/tags/*:refs/tags/* --prune
```

[Source](https://stackoverflow.com/questions/31725436/git-tags-are-showing-even-though-i-deleted-them)

## List Tags

To view all tags:

```bash
git tag
git tag -l v*
```

To view all tags with a wildcard search:

```bash
# View all tags starting with 'v'
git tag -l v*

# View all tags ending with '-rc'
git tag -l *-rc

# View all tags with 'test' somewhere within them
git tag -l *test*
```

### Push Tags

Once create tags can be pushed with:

```bash
git push --tags
```

