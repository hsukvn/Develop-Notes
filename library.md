# Library

### Different kinds of libraries

* .o (obj file) 是目標物件函式庫, 等同於 Windows 的 .obj
* .a 為靜態函式庫, 可以是 一個 或 多個 .o 合在一起, 用於靜態連結
* .so 為動態函式庫, 類似 Windows 的 DLL(Dynamic-link library)檔.


### How to generate libraries
* .o
    ```
    gcc -c test.c
    ```
* .a
    ```
    ar -r libtest.a test1.o test2.o
    ```
* .so
    ```
    gcc -Wall -fpic -shared test1.c test2.c -o libtest.so
    ```