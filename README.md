# cygwin-dotfiles

## Import & Export Cygwin List of installed Packages

### Export

``` bash
cygcheck -c -d | sed -e "1,2d" -e 's/ .*\$//' > packagelist
```

### Import

``` bash
./setup-x86_64.exe -P `awk 'NR==1{printf \$1}{printf ",%s", \$1}' packagelist`
```

## openssh

https://docs.oracle.com/cd/E24628_01/install.121/e22624/preinstall_req_cygwin_ssh.htm
