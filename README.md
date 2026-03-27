# Smart Eye Pro Tools

Smart Eye Pro gaze tracker tools for .NET apps.
Implements a TCP client that receives gaze data.

## Usage

```c#
using var tcpClient = new SmartEyeTools.Client();

tcpClient.Sample += (s, e) => { /* consume data */ }

Exception? ex;
if ((ex = await tcpClient.Connect("127.0.0.1", 5002)) == null) { /* ok */
else { /* could not connect */ }
```
