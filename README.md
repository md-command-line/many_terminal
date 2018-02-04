# mac_open_window_run_command

for d in ./*/ ; do (cd "$d" && echo "$d" && osascript -e 'tell app "Terminal" to do script "echo hello world"'); done;
