# MapReduce

### How to run
```shell
go build -buildmode=plugin ../mrapps/wc.go
go run mrmaster.go pg-*.txt &
go run mrworker.go wc.so
```

---

<a name="EEkIk"></a>
### Framework
![image.png](https://cdn.nlark.com/yuque/0/2020/png/1532622/1597655632942-f18f20c5-a146-4b18-8383-b8827e52e997.png#align=left&display=inline&height=1278&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1278&originWidth=2253&size=775570&status=done&style=none&width=2253)<br />


---

<a name="rqpaJ"></a>
### How to deal with failed tasks?


- When the master does not receive a reply from the worker within 10 seconds or the worker replies that the task has failed, the task is considered a failure.
- Failed tasks will be reassigned to idle workers.


<br />
