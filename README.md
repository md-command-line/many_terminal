# mac_open_window_run_command

```bash 
for d in ./*/ ; do (cd "$d" && echo "$d" && osascript -e 'tell app "Terminal" to do script "echo hello world"'); done;
```

# rewrite, to do the job. But lolz, definately not posix compliant.

```bash 
dir=pwd;for d in */ ; do (cd "$d" && echo "$d" && osascript -e 'tell app "Terminal" to do script "'"echo $($dir)"'"'); done;
```
# There must be another way, [link](https://stackoverflow.com/questions/29510815/how-to-pass-command-line-arguments-to-a-program-run-with-the-open-command)
```bash
echo "echo hello" > /tmp/tmp.sh ; chmod +x /tmp/tmp.sh ; open -a Terminal /tmp/tmp.sh
```
