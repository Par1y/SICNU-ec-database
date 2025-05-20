# 第1关：获取进程常见属性

## 补全getProcInfo函数，用于获取当前进程ID和其父进程ID(提示：将结果存放在procIDInfo结构体中)。

	ret.pid = getpid();
	ret.ppid = getppid();


# 第2关：进程创建操作-fork

## 补全createProcess函数，使用fork函数创建进程，并在子进程中输出"Children"字符串，在父进程中输出"Parent"字符串。(注意：不要在createProcess函数中使用exit函数或者return来退出程序)。

	pid_t pid;
    pid = fork();
	if(pid == -1) {
        printf("");
    }else if(pid == 0){
        printf("Children");
    }else{
        printf("Parent");
    }


# 第3关：进程创建操作-vfork

## 补全createProcess函数，使用vfork函数创建进程，并在子进程中输出"Children"字符串(提示：需要换行)，在父进程中输出"Parent"字符串(提示：需要换行)。

	pid_t pid;
    pid = vfork();
	if(pid == 0) {
        printf("Children\n");
    }else{
        printf("Parent\n");
    }


# 第4关：进程终止

## 补全exitProcess函数，使用atexit函数注册一个函数，在注册函数中打印出当前进程的ID号。

	void a(){ pid_t pid = getpid(); printf("%u", pid); }
	atexit(a);