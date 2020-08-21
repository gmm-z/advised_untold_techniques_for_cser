# tar: Tape Archiver

`tar [OPTION]... [FILE]...`

- lisT: `tar -tavf ARCH.tar.gz`
- Create: `tar -cavf ARCH.tar.gz PATH...`
- eXtract: `tar -xavf ARCH.tar.gz`

- Device/Archive Select
    - `-f ARCHIVE`, `--file=ARCHIVE`: File archive
- Operation
    - `-t`, `--list`
    - `-c`, `--create`
    - `-x`, `--extract`, `--get`
    - `-d`, `--diff`, `--compare`: Diff arch and file
    - `--delete`: Delete file from arch
    - `-r`, `--append`
    - `-u`, `--update`
- Compression Program/Algorithm
    - `-a`, `--[no-]auto-compress`: According to Suffix
    - `-z`, `--g[un]zip`
    - `-I`, `--use-compress-program=PROG`
    - `--lzma`
    - `-Z`, `--[un]compress`
- Filter
    - `--no-recursion`
    - `--exclude=PATTERN`
    - `-X FILE`, `--exclude-from=PATTERN_FILE`
    - `--exclude-(backups|caches[-all|-under])`
    - `--exclude-ignore[-recursive]=PATTERN_FILE_PATH`
    - `--exclude-tag[-all|-under]=FILE`
    - `--exclude-vcs[-ignores]`
    - Pattern
        - `--anchored`: Prefix `^` to pattern
        - `--no-anchored`: Do NOT prefix `^` to pattern (exclusion default)
        - `--ignore-case`
        - `--no-ignore-case` (default)
        - `--wildcards` (exclusion default)
        - `--no-wildcards`: No Metachars
        - `--no-wildcards-match-slash`: Wildcards do NOT match `/`
        - `--wildcards-match-slash`: Wildcards match `/` (exclusion default)
- Log
    - `--index-file=FILE`: Verbose Index
    - `--show-omitted-dirs`
    - `--show-(transformed|stored)-names`
    - `--totals`: Total bytes
    - `-v`, `--verbose`
    - `-w`, `--interactive`, `-confirmation`
- File Name
    - `--transform|xform=EXPR`: `sed` process
- Output Stream
    - `-O`, `--to-stdout`: `stdout` as archive
- File Attribute
    - Time
        - `--atime-preserve[=replace|system]`
        - `--mtime=TIME`
        - `-m`, `--touch`: Set mod time to extracting time
    - Mode
        - `--mode=MODE`
        - `-p`, `--preserve-permisions`, `--same-permissions`: Restore Mode
    - Owner
        - `--numeric-owner`: U/GID instead of Name
        - `--same-owner`: Restore Owner
        - `--no-same-(owner|permissions)`: Set owner/mode to current user's
        - `--owner=NAME`
        - `--owner-map=MAP_FILE`
        - `--group=NAME`
        - `--group-map=MAP_FILE`
    - `--[no-]acls`
    - `--[no-]xattrs[-(in|ex)clude=MASK]`
- Archive Format: `gnu|pax|posix|ustar|`
    - `-H FORMAT`, `--format=FORMAT`