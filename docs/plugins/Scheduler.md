# Task Scheduler

Some people may think that using NodeJS's default functions setTimeout and setInterval is faster. I'm not arguing that it's wrong, but I wanted to create this feature to help users optimize their performance and write better code.


For the Task Scheduler, there are two main methods:
The `scheduleDelayedTask` method: creates a task to be executed after a specific period of time.
The `scheduleDelayedRepeatingTask` method: creates a task that repeats and executes after a specific period of time.

Tick: `1000` would be equivalent to `1` second

Ex:
```js
this.getScheduler().scheduleDelayedTask(new TestTask(), 1000);
this.getScheduler().scheduleDelayedRepeatingTask(new TestTask(), 1000);
```

For `TestTask.js`
```js
export class TestTask extends Task {

    onRun() {
        console.log("Hello World!")
    }
}
```

```{tip}
You can call the `CancelTaskException` to cancel a task while it is being processed. Additionally, you can use the `onCancel` function to do something when that task is canceled.
```