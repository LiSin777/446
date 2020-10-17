# Qinfenfeng
多线程读取文件(通道完成)
思路：
用一个MyTask类来实现Callable，返回值为一个1024 * 8 大小的ByteBuffer，
每个线程都会创建一个1024 * 8大小的ByteBuffer来读取inChannel中文件的
部分数据，然后返回到主线程中给ByteBuffer[]来接受，最后将数组中的数据
写入指定文件。
