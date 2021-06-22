# `Timer`
uv timer.
<br></br>
```C++
Timer(EventLoop* loop, uint64_t timeout, uint64_t repeat, TimerCallback callback)
```
Constructor.
* `EventLoop*` loop : Event loop's handle.
* `int64_t` timeout : The initial timeout in milliseconds.
* `uint64_t` repeat : Timer timeout period, won't repeat, if it is zero.
* `TimerCallback` callback : Timer callback function.

```C++
virtual ~Timer()
```
Destructor.

```C++
void start()
```
Strat the timer.

```C++
void close(TimerCloseComplete callback)
```
Close the timer.
* `TimerCloseComplete` callback : Callback function after close completion, timer object can be safely destroyed in callback.
* `TimerCloseComplete` : `void(Timer*)`.

```C++
void setTimerRepeat(uint64_t ms)
```
Modify the timer period.
* `uint64_t` ms : Timer timeout period in milliseconds.
