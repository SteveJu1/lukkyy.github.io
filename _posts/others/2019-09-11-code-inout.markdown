---
layout:     post
title:      "Java输入输出 "
date:       2019-09-11 
categories: Other
tags: Blog
---



System.in System.out 输出，输出模板





```java
import java.util.*;
import java.io.BufferedReader;
public class Main{
    public static void main(String[] args){
        System.out.println("输入字符")；
        BufferedReader input = new BufferedReader(new InputStream(System.in));
        String str = br.readLine();
        String[] s = str.split(",");
        int [] arr = new int[s.length];
        for(int i=0;i<s.length;i++){
            arr[i] = Integer.valueOf(s[i]);
        }
        
        System.out.println(res);
    }
}
```

Scanner



```java
Scanner xx = new Scanner( System.in );//创建Scanner类型对象，赋给变量xxx
常用方法：
nextByte(); 读取一个byte类型的整数。
nextShort(); 读取一个short类型的整数。
nextInt(); 读取一个int类型的整数。
nextLong(); 读取一个long类型的整数。
nextFloat(); 读取一个float类型的整数。
nextDouble(); 读取一个double类型的整数。
next(); 读取一个字符串，该字符在一个空白符之前结束。
nextLine(); 读取一行文本（即以按下enter键为结束标志）。

```



```
import java.io.IOException;
import java.io.InputStream;
import java.io.OutputStream;
 
public class Demo {
 
	public static void main(String[] args) {
 
		InputStream is = System.in;// 标准的输入流对象 --读取操作
		OutputStream os = System.out;// 标准的输出流对象---写的操作
		try {
			byte[] buffer = new byte[10]; // 缓冲区 // 0 1 2 3 4 5 6 7 8 9
			int len = 0;// 读取之后的实际长度 //在UTF8编码下，回车\r 换行\n 也各占1个字节
			/*
			 * read方法参数： b - 读入数据的缓冲区。 off - 数组 b 中将写入数据的初始偏移量。 len - 要读取的最大字节数。
			 */
			while ((len = is.read(buffer, 0, 4)) != -1) { //读取操作												
				System.out.println("读取的实际长度--------------------------" + len);
				os.write(buffer, 0, 4); //写出的操作
				System.out.println("--------------------------");
			}
		} catch (IOException e) {
			e.printStackTrace();
		}
	}
 
}
```

