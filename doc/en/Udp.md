# Udp
Udp class.
```C++
Udp(EventLoop* loop)
```
Constructor.
* EventLoop* loop : Event loop's handle.

```C++
virtual ~Udp()
```
Destructor.

```C++
int bindAndRead(SocketAddr& addr)
```
Bind address and start read data.
* SocketAddr& addr : The address to read from.
* return : `0` on success, or an error-code `< 0` on failure.

```C++
int send(SocketAddr& to, const char* buf, unsigned size)
```
Send data.
* SocketAddr& to : The target address.
* const char* buf : data buffer to send.
* unsigned size : length of data in buf.
* return : `0` on success, or an error-code `< 0` on failure.

```C++
void close(DefaultCallback callback)
```
Close Udp.
* DefaultCallback callback : Callback function after closing.

```C++
void setMessageCallback(OnUdpMessageCallback callback)
```
Set callback for new message.
* OnUdpMessageCallback callback : Callback function for new messages.
