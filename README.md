# mac_open_window_run_command

```bash 
for d in ./*/ ; do (cd "$d" && echo "$d" && osascript -e 'tell app "Terminal" to do script "echo hello world"'); done;
```

# rewrite, to do the job. But lolz, definately not posix compliant.

```bash 
dir=pwd;for d in */ ; do (cd "$d" && echo "$d" && osascript -e 'tell app "Terminal" to do script "'"echo $($dir)"'"'); done;
```
