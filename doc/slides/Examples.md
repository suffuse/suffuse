# Suffuse Examples

--

## Create

```
> val sfs = sfsImport(/home)         # import "real" filesystem

> val sfs = (p: Path) => generate(p) # write Path=>Node generator

> val sfs = sfsConfig(/foo/bar.sfs)  # configure existing generator

> val sfs = sfs1 op sfs2 op sfs3     # compose existing sfses
```
--

## Filter
```
> sfs without ".DS_Store"

> sfs prune "target"

> sfs.ignoreLikeGit

> sfs where (LastModified.value < 7.days) && Owner.isMe
```
--
## Transform
```
> sfs expand "flac" -> "mp3"

> sfs map ("html" -> tidyHtml)
```
--
## Compose
```
> union(PATH split ':' map sfsImport)

> union(~/Library, /Library, /System/Library)/Preferences
```
--
## Decompose
```
> sfs partitionBy Type

> sfs partitionBy LastModified.date
```
--
## Observe/Validate
```
> sfs logIf (Name =~ "*.conf") && (Action == Write)

> sfs enforceStrict Extension("xml") ==> isValidXml

> sfs enforceInGit Extension("xml") ==> isValidXml
```
