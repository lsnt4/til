# How to Center a jFrame at Startup in Netbeans

Right click `jFrame` -> `Properties` -> `Events` -> `windowOpened` -> ... -> add a handler called `formWindowOpened`  
In that `formWindowOpened` method, paste following code.

```java
setExtendedState(JFrame.MAXIMIZED_BOTH);
```