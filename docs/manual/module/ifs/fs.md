# 模块 fs
文件系统处理模块

使用方法：
```JavaScript
var fs = require('fs');
```
## 函数
        
### exists
查询指定的文件或目录是否存在
```JavaScript
static Boolean fs.exists(String path) async;
```

调用参数:
* path - 指定要查询的路径

返回结果:
* 返回 True 表示文件或目录存在

--------------------------
### existsSync
查询指定的文件或目录是否存在，是 exists 的同步版兼容接口
```JavaScript
static Boolean fs.existsSync(String path);
```

调用参数:
* path - 指定要查询的路径

返回结果:
* 返回 True 表示文件或目录存在

--------------------------
### access
查询用户对指定的文件的权限
```JavaScript
static fs.access(String path,
                Integer mode = 0) async;
```

调用参数:
* path - 指定要查询的路径
* mode - 指定查询的权限,默认为文件是否存在

--------------------------
### accessSync
查询用户对指定的文件的权限, accesss同步兼容版本
```JavaScript
static fs.accessSync(String path,
                Integer mode = 0);
```

调用参数:
* path - 指定要查询的路径
* mode - 指定查询的权限,默认为文件是否存在

--------------------------
### link
创建硬链接文件, windows 下不支持此方法
```JavaScript
static fs.link(String oldPath,
                String newPath) async;
```

调用参数:
* oldPath - 源文件
* newPath - 将要被创建的文件

--------------------------
### linkSync
创建硬链接文件，windows 下不支持此方法，是 link 的同步版兼容接口
```JavaScript
static fs.linkSync(String oldPath,
                String newPath);
```

调用参数:
* oldPath - 源文件
* newPath - 将要被创建的文件

--------------------------
### unlink
删除指定的文件
```JavaScript
static fs.unlink(String path) async;
```

调用参数:
* path - 指定要删除的路径

--------------------------
### unlinkSync
删除指定的文件，是 unlink 的同步版兼容接口
```JavaScript
static fs.unlinkSync(String path);
```

调用参数:
* path - 指定要删除的路径

--------------------------
### mkdir
创建一个目录
```JavaScript
static fs.mkdir(String path,
                Integer mode = 0777) async;
```

调用参数:
* path - 指定要创建的目录名
* mode - 指定文件权限，Windows 忽略此参数

--------------------------
### mkdirSync
创建一个目录，是 mkdir 的同步版兼容接口
```JavaScript
static fs.mkdirSync(String path,
                Integer mode = 0777);
```

调用参数:
* path - 指定要创建的目录名
* mode - 指定文件权限，Windows 忽略此参数

--------------------------
### rmdir
删除一个目录
```JavaScript
static fs.rmdir(String path) async;
```

调用参数:
* path - 指定要删除的目录名

--------------------------
### rmdirSync
删除一个目录，是 rmdir 的同步版兼容接口
```JavaScript
static fs.rmdirSync(String path);
```

调用参数:
* path - 指定要删除的目录名

--------------------------
### rename
重新命名一个文件
```JavaScript
static fs.rename(String from,
                String to) async;
```

调用参数:
* from - 指定更名的文件
* to - 指定要修改的新文件名

--------------------------
### renameSync
重新命名一个文件，是 rename 的同步版兼容接口
```JavaScript
static fs.renameSync(String from,
                String to);
```

调用参数:
* from - 指定更名的文件
* to - 指定要修改的新文件名

--------------------------
### copy
复制一个文件
```JavaScript
static fs.copy(String from,
                String to) async;
```

调用参数:
* from - 指定更名的文件
* to - 指定要修改的新文件名

--------------------------
### chmod
设置指定文件的访问权限，Windows 不支持此方法
```JavaScript
static fs.chmod(String path,
                Integer mode) async;
```

调用参数:
* path - 指定操作的文件
* mode - 指定设定的访问权限

--------------------------
### chmodSync
设置指定文件的访问权限，是 chmod 的同步版兼容接口
```JavaScript
static fs.chmodSync(String path,
                Integer mode);
```

调用参数:
* path - 指定操作的文件
* mode - 指定设定的访问权限

--------------------------
### lchmod
设置指定文件的访问权限，若文件是软连接则不改变指向文件的权限，Windows 不支持此方法
```JavaScript
static fs.lchmod(String path,
                Integer mode) async;
```

调用参数:
* path - 指定操作的文件
* mode - 指定设定的访问权限

--------------------------
### lchmodSync
设置指定文件的访问权限，若文件是软连接则不改变指向文件的权限，是 lchmod 的同步版兼容接口
```JavaScript
static fs.lchmodSync(String path,
                Integer mode);
```

调用参数:
* path - 指定操作的文件
* mode - 指定设定的访问权限

--------------------------
### chown
设置指定文件的拥有者，Windows 不支持此方法
```JavaScript
static fs.chown(String path,
                Integer uid,
                Integer gid) async;
```

调用参数:
* path - 指定设置的文件
* uid - 文件拥有者用户id
* gid - 文件拥有者组id

--------------------------
### chownSync
设置指定文件的拥有者，Windows 不支持此方法, 是 chown 的同步版兼容接口
```JavaScript
static fs.chownSync(String path,
                Integer uid,
                Integer gid);
```

调用参数:
* path - 指定设置的文件
* uid - 文件拥有者用户id
* gid - 文件拥有者组id

--------------------------
### lchown
设置指定文件的拥有者，如果指定的文件是软连接则不会改变其指向文件的拥有者，Windows 不支持此方法
```JavaScript
static fs.lchown(String path,
                Integer uid,
                Integer gid) async;
```

调用参数:
* path - 指定设置的文件
* uid - 文件拥有者用户id
* gid - 文件拥有者组id

--------------------------
### lchownSync
设置指定文件的拥有者，如果指定的文件是软连接则不会改变其指向文件的拥有者，Windows 不支持此方法, 是 lchown 的同步版兼容接口
```JavaScript
static fs.lchownSync(String path,
                Integer uid,
                Integer gid);
```

调用参数:
* path - 指定设置的文件
* uid - 文件拥有者用户id
* gid - 文件拥有者组id

--------------------------
### stat
查询指定文件的基础信息
```JavaScript
static Stat fs.stat(String path) async;
```

调用参数:
* path - 指定查询的文件

返回结果:
* 返回文件的基础信息

--------------------------
### statSync
查询指定文件的基础信息，是 stat 的同步版兼容接口
```JavaScript
static Stat fs.statSync(String path);
```

调用参数:
* path - 指定查询的文件

返回结果:
* 返回文件的基础信息

--------------------------
### lstat
查询指定文件的基础信息, 和stat不同的是, 当[path](path.md)是一个软连接的时候，返回的将是这个软连接的信息而不是指向的文件的信息
```JavaScript
static Stat fs.lstat(String path) async;
```

调用参数:
* path - 指定查询的文件

返回结果:
* 返回文件的基础信息

--------------------------
### lstatSync
查询指定文件的基础信息，是 lstat 的同步版兼容接口
```JavaScript
static Stat fs.lstatSync(String path);
```

调用参数:
* path - 指定查询的文件

返回结果:
* 返回文件的基础信息

--------------------------
### readlink
读取指定的软连接文件, windows 下不支持此方法
```JavaScript
static String fs.readlink(String path) async;
```

调用参数:
* path - 指定读取的软连接文件

返回结果:
* 返回软连接指向的文件名

--------------------------
### readlinkSync
读取指定的软连接文件，windows 下不支持此方法，是 readlink 的同步版兼容接口
```JavaScript
static String fs.readlinkSync(String path);
```

调用参数:
* path - 指定读取的软连接文件

返回结果:
* 返回软连接指向的文件名

--------------------------
### realpath
返回指定路径的绝对路径，如果指定路径中包含相对路径也会被展开
```JavaScript
static String fs.realpath(String path) async;
```

调用参数:
* path - 指定读取的路径

返回结果:
* 返回处理后的绝对路径

--------------------------
### realpathSync
返回指定路径的绝对路径，如果指定路径中包含相对路径也会被展开，是 realpath 的同步版兼容接口
```JavaScript
static String fs.realpathSync(String path);
```

调用参数:
* path - 指定读取的路径

返回结果:
* 返回处理后的绝对路径

--------------------------
### symlink
创建软连接文件
```JavaScript
static fs.symlink(String target,
                String linkpath) async;
```

调用参数:
* target - 目标文件，可以是文件、目录、或不存在的路径
* linkpath - 将被创建的软连接文件

--------------------------
### symlinkSync
创建软连接文件, 是 symlink 的同步版兼容接口
```JavaScript
static fs.symlinkSync(String target,
                String linkpath);
```

调用参数:
* target - 目标文件，可以是文件、目录、或不存在的路径
* linkpath - 将被创建的软连接文件

--------------------------
### truncate
修改文件尺寸,如果指定的长度大于源文件大小则用'\0'填充，否则多于的文件内容将丢失
```JavaScript
static fs.truncate(String path,
                Integer len) async;
```

调用参数:
* path - 指定被修改文件的路径
* len - 指定修改后文件的大小

--------------------------
### truncateSync
修改文件尺寸,如果指定的长度大于源文件大小则用'\0'填充，否则多于的文件内容将丢失，是 truncate 的同步版兼容接口
```JavaScript
static fs.truncateSync(String path,
                Integer len);
```

调用参数:
* path - 指定被修改文件的路径
* len - 指定修改后文件的大小

--------------------------
### readdir
读取指定目录的文件信息
```JavaScript
static List fs.readdir(String path) async;
```

调用参数:
* path - 指定查询的目录

返回结果:
* 返回目录的文件信息数组

--------------------------
### readdirSync
读取指定目录的文件信息，是 readdir 的同步版兼容接口
```JavaScript
static List fs.readdirSync(String path);
```

调用参数:
* path - 指定查询的目录

返回结果:
* 返回目录的文件信息数组

--------------------------
### open
打开文件，用于读取，写入，或者同时读写
```JavaScript
static SeekableStream fs.open(String fname,
                String flags = "r") async;
```

调用参数:
* fname - 指定文件名
* flags - 指定文件打开方式，缺省为 "r"，只读方式

返回结果:
* 返回打开的文件对象

参数 flags 支持的方式如下：
- 'r' 只读方式，文件不存在则抛出错误。
- 'r+' 读写方式，文件不存在则抛出错误。
- 'w' 只写方式，文件不存在则自动创建，存在则将被清空。
- 'w+' 读写方式，文件不存在则自动创建。
- 'a' 只写添加方式，文件不存在则自动创建。
- 'a+' 读写添加方式，文件不存在则自动创建。

--------------------------
### openSync
打开文件，用于读取，写入，或者同时读写，是 open 的同步版兼容接口
```JavaScript
static SeekableStream fs.openSync(String fname,
                String flags = "r");
```

调用参数:
* fname - 指定文件名
* flags - 指定文件打开方式，缺省为 "r"，只读方式

返回结果:
* 返回打开的文件对象

参数 flags 支持的方式如下：
- 'r' 只读方式，文件不存在则抛出错误。
- 'r+' 读写方式，文件不存在则抛出错误。
- 'w' 只写方式，文件不存在则自动创建，存在则将被清空。
- 'w+' 读写方式，文件不存在则自动创建。
- 'a' 只写添加方式，文件不存在则自动创建。
- 'a+' 读写添加方式，文件不存在则自动创建。

--------------------------
### openTextStream
打开文本文件，用于读取，写入，或者同时读写
```JavaScript
static BufferedStream fs.openTextStream(String fname,
                String flags = "r") async;
```

调用参数:
* fname - 指定文件名
* flags - 指定文件打开方式，缺省为 "r"，只读方式

返回结果:
* 返回打开的文件对象

参数 flags 支持的方式如下：
- 'r' 只读方式，文件不存在则抛出错误。
- 'r+' 读写方式，文件不存在则抛出错误。
- 'w' 只写方式，文件不存在则自动创建，存在则将被清空。
- 'w+' 读写方式，文件不存在则自动创建。
- 'a' 只写添加方式，文件不存在则自动创建。
- 'a+' 读写添加方式，文件不存在则自动创建。

--------------------------
### readTextFile
打开文本文件，并读取内容
```JavaScript
static String fs.readTextFile(String fname) async;
```

调用参数:
* fname - 指定文件名

返回结果:
* 返回文件文本内容

--------------------------
### readFile
打开二进制文件，并读取内容
```JavaScript
static Buffer fs.readFile(String fname) async;
```

调用参数:
* fname - 指定文件名

返回结果:
* 返回文件文本内容

--------------------------
### readFileSync
打开二进制文件，并读取内容，是 readFile 的同步版兼容接口
```JavaScript
static Buffer fs.readFileSync(String fname);
```

调用参数:
* fname - 指定文件名

返回结果:
* 返回文件文本内容

--------------------------
### readLines
打开文件，以数组方式读取一组文本行，行结尾标识基于 EOL 属性的设置，缺省时，posix:"\n"；windows:"\r\n"
```JavaScript
static Array fs.readLines(String fname,
                Integer maxlines = -1);
```

调用参数:
* fname - 指定文件名
* maxlines - 指定此次读取的最大行数，缺省读取全部文本行

返回结果:
* 返回读取的文本行数组，若无数据可读，或者连接中断，空数组

--------------------------
### writeTextFile
创建文本文件，并写入内容
```JavaScript
static fs.writeTextFile(String fname,
                String txt) async;
```

调用参数:
* fname - 指定文件名
* txt - 指定要写入的字符串

--------------------------
### writeFile
创建二进制文件，并写入内容
```JavaScript
static fs.writeFile(String fname,
                Buffer data) async;
```

调用参数:
* fname - 指定文件名
* data - 指定要写入的二进制数据

--------------------------
### writeFileSync
创建二进制文件，并写入内容，是 writeFile 的同步版兼容接口
```JavaScript
static fs.writeFileSync(String fname,
                Buffer data);
```

调用参数:
* fname - 指定文件名
* data - 指定要写入的二进制数据

--------------------------
### appendFile
创建二进制文件，并写入内容
```JavaScript
static fs.appendFile(String fname,
                Buffer data) async;
```

调用参数:
* fname - 指定文件名
* data - 指定要写入的二进制数据

--------------------------
### appendFileSync
创建二进制文件，并写入内容，是 appendFile 的同步版兼容接口
```JavaScript
static fs.appendFileSync(String fname,
                Buffer data);
```

调用参数:
* fname - 指定文件名
* data - 指定要写入的二进制数据

## 属性
        
### constants
fs模块的常量对象
```JavaScript
static readonly Object fs.constants;
```

## 常量
        
### SEEK_SET
seek 方式常量，移动到绝对位置
```JavaScript
const fs.SEEK_SET = 0;
```

--------------------------
### SEEK_CUR
seek 方式常量，移动到当前位置的相对位置
```JavaScript
const fs.SEEK_CUR = 1;
```

--------------------------
### SEEK_END
seek 方式常量，移动到文件结尾的相对位置
```JavaScript
const fs.SEEK_END = 2;
```
