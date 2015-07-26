# npmfreeze
pip freeze for nodejs.


Add this to bashrc:
```
npmfreeze(){
  npm ls | grep -E "^(├|└)─" | cut -d" " -f2 | awk '{FS = "@"; print "\""$1"\"", ":", "\""$2"\""}'
}
```


then execute:
```
source ~/.bashrc
```
