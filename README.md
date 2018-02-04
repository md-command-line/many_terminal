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
### test out later, [link](https://stackoverflow.com/questions/17302977/how-to-launch-git-bash-from-dos-command-line)
```bash 
start "" "%ProgramFiles%\Git\git-bash.exe" -c "echo 1 && echo 2 && /usr/bin/bash --login -i"
```
```bash
start "" "c:\path with spaces\app.exe" param1 "param with spaces"
```
