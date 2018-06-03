1。java的线程开启，默认的虚拟机会分配1M的内存，但是在4G的windows上线程最多也就开到300多 ，是因为windows本身的一些限制导致。
2。虚拟机给每个线程分配的内存（栈空间）是由虚拟机参数-Xss来指定的，在不同平台上对应的默认大小可以 在oracle的官方文档上查询到：
http://docs.oracle.com/cd/E13150_01/jrockit_jvm/jrockit/jrdocs/refman /optionX.html
其中，Linux64位默认Xss值为256K，并非1M或10M
3。一个Java进程可以启动的线程数可以通过如下公式计算：
     （系统剩余内存 - 最大堆容量Xmx - 最大方法区容量MaxPermSize）／ 最大栈空间Xss
这样，4G的服务器单个进程可以开多少线程，可以粗略计算出来，大概是5000个线程。