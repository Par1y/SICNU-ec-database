# 互斥锁

## 补全ThreadHandler函数中代码，使用互斥锁对position和buffer变量加锁，使其同一时刻只能被一个线程访问。

    pthread_mutex_lock(&mutex);

    pthread_mutex_unlock(&mutex);


# 自旋锁

## 补全ThreadHandler函数中代码，使用自旋锁对position和buffer变量加锁，使其同一时刻只能被一个线程访问。

    pthread_spin_lock(&lock);

    pthread_spin_unlock(&lock);


# 条件变量

## 补全ThreadHandler1和ThreadHandler2函数中代码.ThreadHandler1函数中对position变量进行加一操作(只有一个线程使用，无需加锁)，当position变量被加一后，则只通知一个线程执行ThreadHandler2函数完成字符串赋值操作。

    pthread_cond_signal(&cond);

    pthread_cond_wait(&cond,&mutex);

    pthread_mutex_unlock(&mutex);


# 项目实战

## 补全Consumer函数，该函数是用来消费由生产者产生的数据。

    pthread_mutex_lock( & mutex);
    while (beginData == NULL) {
      pthread_cond_wait( & cond, & mutex);
    }
    if (beginData - > number == -1) {
      pthread_mutex_unlock( & mutex);
      pthread_exit(NULL);
    }
    //消费数据
    printf("%d\n", beginData - > number);
    consumer_number++;
    //将消费后的数据释放掉
    struct msg * tmp = beginData;
    beginData = beginData - > next;
    free(tmp);
    pthread_mutex_unlock( & mutex);