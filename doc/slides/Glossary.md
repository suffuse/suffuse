# Suffuse Glossary

| Term | Meaning                   |
| ---- | -------------             |
| Name | constrained string        |
| Path | string => 0+ Names        |
| Node | file, dir, link, etc      |
| UKey | name-independent Node key |

--

| Node | Synonym           | Primary Data    |
| ---- | -------------     | --------------  |
| Dir  | directory/folder  | Map[Name, Node] |
| File | regular file      | Bytes           |
| Link | symbolic link     | Path            |
| Comm | pipe, socket, etc | Channel         |

--

| Term | Description        | Example             |
| ---- | -------------      | --------------      |
| FS   | Path => Node       | /foo -> Text("abc") |
| AFS  | mounted atomic FS  | /dev/disk2 at /mnt1 |
| SFS  | mounted suffuse FS | myFs at /mnt2       |
