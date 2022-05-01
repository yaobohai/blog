---
title: SHELL脚本捷径库

index_img: https://itsfoss.com/wp-content/uploads/2021/09/bash-command-not-found-error-1.png
---

## 记录下常用的代码段

### 判断命令是否存在

```shell
# 例如: docker命令
export cmd='docker'
if [ ! `command -v ${cmd}` ];then echo "${cmd} not install";exit 1;fi
```

### 批量创建文件夹方法
```shell
function make_dir() {
  local dirs=(
      # 文件夹01
      '/root/dir01/'
      # 文件夹02
      '/etc/dir02/'
  )
  local dirs_num=${#dirs[@]}
  for ((i=0;i<dirs_num;i++));{ mkdir -p ${dirs[i]} ;}
}

# 记得调用方法
make_dir
```
