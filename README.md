# mac_new_terminalwindow_run_command
# Windows Solution, [link](https://stackoverflow.com/questions/17302977/how-to-launch-git-bash-from-dos-command-line)
```bash
for d in ./*/; do (cd "$d" && echo "$d" && start sh -c "echo $d; git status;"); done;
```
```bash 
start "" "%ProgramFiles%\Git\git-bash.exe" -c "echo 1 && echo 2 && /usr/bin/bash --login -i"
```
```bash
start "" "c:\path with spaces\app.exe" param1 "param with spaces"
```
# Mac Solution
```bash 
dir=pwd;for d in */ ; do (cd "$d" && echo "$d" && osascript -e 'tell app "Terminal" to do script "'"echo $($dir)"'"'); done;
```
# There must be another way, Mac and Linux? [link](https://stackoverflow.com/questions/29510815/how-to-pass-command-line-arguments-to-a-program-run-with-the-open-command)
```bash
echo "echo hello" > /tmp/tmp.sh ; chmod +x /tmp/tmp.sh ; open -a Terminal /tmp/tmp.sh
```
