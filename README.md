# YASGCDTimerManager
## 利用GCD实现的定时器
* 可实现管理多个任务
* 可实现设置任务keyName

## Usage example 
```objc
    dispatch_queue_t queue = dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0);;
    LKWeakSelf;
    [[YASGCDTimerManager sharedInstance]scheduledDispatchTimerWithName:@"YASScreenCaptureTool"
                                                          timeInterval:frameRate
                                                                 queue:queue
                                                               repeats:YES
                                                          actionOption:YASGCDTimerManagerAbandonPreviousAction
                                                                action:^{
         /** 定时执行的任务**/
    }];
    
    
    /** 取消释放任务*/
    [[YASGCDTimerManager sharedInstance]cancelTimerWithName:@"YASScreenCaptureTool"];
    
    ```
