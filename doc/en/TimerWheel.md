# `TimerWheel template<typename Type>`
Time wheel.

### Constructor
```C++
TimerWheel(EventLoop* loop)
```
* `EventLoop*` loop : Event loop's handle.
<br/><br/>
```C++
TimerWheel(EventLoop* loop, unsigned int timeout)
```
* `EventLoop*` loop : Event loop's handle.
* `unsigned int` timeout : Timeout in seconds.

### `setTimeout`
```C++
void setTimeout(unsigned int seconds)
```
Set timeout of seconds.
* `unsigned int` timeout : Timeout in seconds.

### `getTimeout`
```C++
int getTimeout()
```
Get timeout of seconds.
* return : Timeout in seconds.

### `start`
```C++
void start()
```
Start time wheel.

### `insert`
```C++
void insert(std::shared_ptr<Type> value)
```
Insert element into time wheel.
* `std::shared_ptr<Type>` value : Elements of the time wheel.
