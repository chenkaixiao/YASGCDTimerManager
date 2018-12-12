YASGCDTimerManager

==============

**YASGCDTimerManager is a  Timer with GCD  for iOS.**  

## Features
- [x] 	 可实现管理多个任务
- [x] 	 可实现管理关键字key管理任务
- [x] 	 性能比NSTimer好

## Usage example 
```objc
    dispatch_queue_t queue = dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0);;
    LKWeakSelf;
    [[YASGCDTimerManager sharedInstance]scheduledDispatchTimerWithName:@"task_1"
                                                          timeInterval:10
                                                                 queue:queue
                                                               repeats:YES
                                                          actionOption:YASGCDTimerManagerAbandonPreviousAction
                                                                action:^{
         /** 定时执行的任务**/
    }];
    
    
    /** 取消释放任务*/
    [[YASGCDTimerManager sharedInstance]cancelTimerWithName:@"task_1"];
    
 ```
