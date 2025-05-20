# Linux之文件创建/删除

## 新创建两个文件空文件file1和file2；
## 删除系统已存在的两个文件oldFile1和oldFile2。

    touch file1 file2
    rm oldFile1 oldFile2


# Linux之目录创建/删除

## 新创建两个空目录newDir1和newDir2；
## 删除系统已存在的两个目录oldDir1和oldDir2，其中oldDir1目录为空、oldDir2目录不为空。

    mkdir newDir1
    mkdir newDir2
    rmdir oldDir1
    rm -r oldDir2


# Linux之文件复制/重命名

## 将当前目录下的文件file1和file2拷贝到目录Dir下；
## 将当前目录下的文件file1拷贝到目录Dir下并重命名为file1Cpy；
## 将当前目录下的文件file3和file4移动到目录Dir下；
## 将当前目录下的文件file5重命名为file6。

    cp file1 file2 Dir/
    cp file1 Dir/file1Cpy
    mv file3 file4 Dir/
    mv file5 file6


# Linux之目录复制/重命名

## 将当前目录下的目录Dir1和Dir2拷贝到目录Dir下；
## 将当前目录下的目录Dir1拷贝到目录Dir下并重命名为Dir1Cpy；
## 将当前目录下的目录Dir3和Dir4移动到目录Dir下；
## 将当前目录下的目录Dir5重命名为Dir6。

    cp -r Dir1 Dir2 Dir/
    cp -r Dir1 Dir/Dir1Cpy
    mv Dir3 Dir4 Dir/
    mv Dir5 Dir6


# Linux之文件/目录内容查看

## 查看当前目录下的文件file1的所有内容；
## 查看当前目录下的文件file2的头5行内容；
## 查看当前目录下的文件file2的末尾5行内容；
## 查看目录/home目录下的所有内容(包括隐藏内容)。

    cat file1
    head -n 5 file2
    tail -n 5 file2
    ls -a /home