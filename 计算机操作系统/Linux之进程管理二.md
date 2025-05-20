# 进程等待

## 补全waitProcess函数，等待子进程结束，并且返回子进程的退出的代码。

    if(waitpid(-1, &status, 0) != -1) {
        if(WIFEXITED(status)) return WEXITSTATUS(status);
    }


# 进程创建操作-exec函数族

## 补全execlProcess函数，使用vfork函数创建进程，并在子进程中调用创建一个名为testDir的目录，在父进程中输出"Parent Process"字符串。

    if(execl("mkdir","mkdir","testDir",NULL) < 0) {
        exit(-1);
    }
    exit(1);

    puts("Parent Process");


# 进程创建操作-system

## 补全createProcess函数，使用system函数创建一个名为testDir的目录(** 调用成功返回命令的状态码，失败返回-1**)。

	int r = system("mkdir testDir");


# 实现一个简单的命令解析器

## 补全RShell函数，实现一个简单的命令解析器工具。(提示：可以使用system函数或者fork+exec+wait。)

	int i = 0;
    while(i < commandNum) {
        int r = system(cmd[i]);
        i++;
    }