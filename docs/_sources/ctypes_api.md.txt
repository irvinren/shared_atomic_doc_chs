# ctypes API 参考

16 种数字类型的 ctype 可以有原子操作函数, 这些类型包括:

|原始ctype        | 原子函数 functions|
| -------------- | ---------------- |
| c_bool         | bool_*           |
| c_byte         | byte_*           |
| c_wchar        | wchar_*          |
| c_ubyte        | ubyte_*          |
| c_short        | short_*          |
| c_ushort       | ushort_*         |
| c_int          | int_*            |
| c_uint         | uint_*           |
| c_long         | long_*           |
| c_ulong        | ulong_*          |
| c_longlong     | longlong_*       |
| c_ulonglong    | ulonglong_*      |
| c_size_t       | size_t_*         |
| c_ssize_t      | ssize_t_*        |
| c_float        | float_store      |
| c_double       | double_store     |
| c_longdouble   | longdouble_store |

## shared_atomic.loaddll()

```{eval-rst}
 .. automodule:: shared_atomic
    :members:
```

## 整数类型支持18 种API 可以用来实现原子操作, 
- 原子获取

  *type*_load(*type* *);

- 原子存储,将b指针当中的内容放入a指针

  *type*_store(*type* *a, *type* *b);

- 原子获取和设置

  *type* *type*_get_and_set(*type* *, *type*);

- 原子比较和设置

  *type* *type*_compare_and_set(*type* *, *type* *, *type*);
  
- 3个指针之间两两交换值, 将a存入c然后将b存入a

  *type*_shift(*type* *a, *type* *b, *type* *c);

- 原子增加和获取

  _Bool *type*_add_and_fetch(*type* *, *type*);

- 原子减少和获取

  *type* *type*_sub_and_fetch(*type* *, *type*);

- 原子"与"和获取

  *type* *type*_and_and_fetch(*type* *, *type*);
  
- 原子"或"和获取

  *type* *type*_or_and_fetch(*type* *, *type*);
  
- 原子"异或"和获取

  *type* *type*_xor_and_fetch(*type* *, *type*);
  
- 原子"与非"和获取

  *type* *type*_nand_and_fetch(*type* *, *type*);
  
- 原子获取和增加

  _Bool *type*_fetch_and_add(*type* *, *type*);

- 原子获取和增加

  *type* *type*_fetch_and_sub(*type* *, *type*);

- 原子获取和"与"

  *type* *type*_fetch_and_and(*type* *, *type*);
  
- 原子获取和"或"

  *type* *type*_fetch_and_or(*type* *, *type*);
  
- 原子获取和"异或"

  *type* *type*_fetch_and_xor(*type* *, *type*);
  
- 原子获取和"与非"

  *type* *type*_fetch_and_nand(*type* *, *type*);

浮点型只支持一种操作, 

- 原子存储,将b指针当中的内容放入a指针

  *type*_store(*type* *, *type* *);

## 布尔原子函数:

`void bool_load(_Bool *);`

`void bool_store(_Bool *, _Bool *);`

`_Bool bool_get_and_set(_Bool *, _Bool);`

`_Bool bool_compare_and_set(_Bool *, _Bool *, _Bool);`

`void bool_shift(_Bool *v, _Bool *, _Bool *);`

## 字节原子函数:

`void byte_load(char *);`

`void byte_store(char *, char *);`

`char byte_get_and_set(char *, char);`

`void byte_shift(char *v, char *, char*);`

`_Bool byte_compare_and_set(char *, char *, char);`

`char byte_add_and_fetch(char *, char);`

`char byte_sub_and_fetch(char *, char);`

`char byte_and_and_fetch(char *, char);`

`char byte_or_and_fetch(char *, char);`

`char byte_xor_and_fetch(char *, char);`

`char byte_nand_and_fetch(char *, char);`

`char byte_fetch_and_add(char *, char);`

`char byte_fetch_and_sub(char *, char);`

`char byte_fetch_and_and(char *, char);`

`char byte_fetch_and_or(char *, char);`

`char byte_fetch_and_xor(char *, char);`

`char byte_fetch_and_nand(char *, char);`

## 无符号字节原子函数:

`void ubyte_load(unsigned char *);`

`void ubyte_store(unsigned char *, unsigned char *);`

`unsigned char ubyte_get_and_set(unsigned char *, unsigned char);`

`void ubyte_shift(unsigned char *, unsigned char *, unsigned char *);`

`_Bool ubyte_compare_and_set(unsigned char *, unsigned char *, unsigned char);`

`unsigned char ubyte_add_and_fetch(unsigned char *, unsigned char);`

`unsigned char ubyte_sub_and_fetch(unsigned char *, unsigned char);`

`unsigned char ubyte_and_and_fetch(unsigned char *, unsigned char);`

`unsigned char ubyte_or_and_fetch(unsigned char *, unsigned char);`

`unsigned char ubyte_xor_and_fetch(unsigned char *, unsigned char);`

`unsigned char ubyte_nand_and_fetch(unsigned char *, unsigned char);`

`unsigned char ubyte_fetch_and_add(unsigned char *, unsigned char);`

`unsigned char ubyte_fetch_and_sub(unsigned char *, unsigned char);`

`unsigned char ubyte_fetch_and_and(unsigned char *, unsigned char);`

`unsigned char ubyte_fetch_and_or(unsigned char *, unsigned char);`

`unsigned char ubyte_fetch_and_xor(unsigned char *, unsigned char);`

`unsigned char ubyte_fetch_and_nand(unsigned char *, unsigned char);`


## 短整型原子函数:

`void short_load(short *);`

`void short_store(short *, short *);`

`short short_get_and_set(short *, short);`

`void short_shift(short *v, short *, short *);`

`_Bool short_compare_and_set(short *, short *, short);`

`short short_add_and_fetch(short *, short);`

`short short_sub_and_fetch(short *, short);`

`short short_and_and_fetch(short *, short);`

`short short_or_and_fetch(short *, short);`

`short short_xor_and_fetch(short *, short);`

`short short_nand_and_fetch(short *, short);`

`short short_fetch_and_add(short *, short);`

`short short_fetch_and_sub(short *, short);`

`short short_fetch_and_and(short *, short);`

`short short_fetch_and_or(short *, short);`

`short short_fetch_and_xor(short *, short);`

`short short_fetch_and_nand(short *, short);`

## 无符号短整型原子函数:

`void ushort_load(unsigned short *);`

`void ushort_store(unsigned short *, unsigned short *);`

`unsigned short ushort_get_and_set(unsigned short *, unsigned short);`

`void ushort_shift(unsigned short *, unsigned short *, unsigned short *);`

`_Bool ushort_compare_and_set(unsigned short *, unsigned short *, unsigned short);`

`unsigned short ushort_add_and_fetch(unsigned short *, unsigned short);`

`unsigned short ushort_sub_and_fetch(unsigned short *, unsigned short);`

`unsigned short ushort_and_and_fetch(unsigned short *, unsigned short);`

`unsigned short ushort_or_and_fetch(unsigned short *, unsigned short);`

`unsigned short ushort_xor_and_fetch(unsigned short *, unsigned short);`

`unsigned short ushort_nand_and_fetch(unsigned short *, unsigned short);`

`unsigned short ushort_fetch_and_add(unsigned short *, unsigned short);`

`unsigned short ushort_fetch_and_sub(unsigned short *, unsigned short);`

`unsigned short ushort_fetch_and_and(unsigned short *, unsigned short);`

`unsigned short ushort_fetch_and_or(unsigned short *, unsigned short);`

`unsigned short ushort_fetch_and_xor(unsigned short *, unsigned short);`

`unsigned short ushort_fetch_and_nand(unsigned short *, unsigned short);`

## 整型原子函数:

`void int_load(int *);`

`void int_store(int *, int *);`

`int int_get_and_set(int *, int);`

`void int_shift(int *, int *, int* );`

`_Bool int_compare_and_set(int *, int *, int);`

`int int_add_and_fetch(int *, int);`

`int int_sub_and_fetch(int *, int);`

`int int_and_and_fetch(int *, int);`

`int int_or_and_fetch(int *, int);`

`int int_xor_and_fetch(int *, int);`

`int int_nand_and_fetch(int *, int);`

`int int_fetch_and_add(int *, int);`

`int int_fetch_and_sub(int *, int);`

`int int_fetch_and_and(int *, int);`

`int int_fetch_and_or(int *, int);`

`int int_fetch_and_xor(int *, int);`

`int int_fetch_and_nand(int *, int);`

## 无符号整型原子函数:

`void uint_load(unsigned int *);`

`void uint_store(unsigned int *, unsigned int *);`

`unsigned int uint_get_and_set(unsigned int *, unsigned int);`

`void uint_shift(unsigned int *, unsigned int *, unsigned int *);`

`_Bool uint_compare_and_set(unsigned int *, unsigned int *, unsigned int);`

`unsigned int uint_add_and_fetch(unsigned int *, unsigned int);`

`unsigned int uint_sub_and_fetch(unsigned int *, unsigned int);`

`unsigned int uint_and_and_fetch(unsigned int *, unsigned int);`

`unsigned int uint_or_and_fetch(unsigned int *, unsigned int);`

`unsigned int uint_xor_and_fetch(unsigned int *, unsigned int);`

`unsigned int uint_nand_and_fetch(unsigned int *, unsigned int);`

`unsigned int uint_fetch_and_add(unsigned int *, unsigned int);`

`unsigned int uint_fetch_and_sub(unsigned int *, unsigned int);`

`unsigned int uint_fetch_and_and(unsigned int *, unsigned int);`

`unsigned int uint_fetch_and_or(unsigned int *, unsigned int);`

`unsigned int uint_fetch_and_xor(unsigned int *, unsigned int);`

`unsigned int uint_fetch_and_nand(unsigned int *, unsigned int);`

## 宽字符型原子函数:

`void wchar_load(wchar_t *);`

`void wchar_store(wchar_t *, wchar_t *);`

`wchar_t wchar_get_and_set(wchar_t *, wchar_t);`

`void wchar_shift(wchar_t *, wchar_t *, wchar_t*);`

`_Bool wchar_compare_and_set(wchar_t *, wchar_t *, wchar_t);`

`wchar_t wchar_add_and_fetch(wchar_t *, wchar_t);`

`wchar_t wchar_sub_and_fetch(wchar_t *, wchar_t);`

`wchar_t wchar_fetch_and_add(wchar_t *, wchar_t);`

`wchar_t wchar_fetch_and_sub(wchar_t *, wchar_t);`

## 长整型原子函数(Linux/MacOSX上是64位，Windows上是32位):

`void long_load(long *);`

`void long_store(long *, long *);`

`void long_shift(long *, long *, long*);`

`long long_get_and_set(long *, long);`

`_Bool long_compare_and_set(long *, long *, long);`

`long long_add_and_fetch(long *, long);`

`long long_sub_and_fetch(long *, long);`

`long long_and_and_fetch(long *, long);`

`long long_or_and_fetch(long *, long);`

`long long_xor_and_fetch(long *, long);`

`long long_nand_and_fetch(long *, long);`

`long long_fetch_and_add(long *, long);`

`long long_fetch_and_sub(long *, long);`

`long long_fetch_and_and(long *, long);`

`long long_fetch_and_or(long *, long);`

`long long_fetch_and_xor(long *, long);`

`long long_fetch_and_nand(long *, long);`

## 无符号长整型原子函数(Linux/MacOSX上是64位，Windows上是32位):

`void ulong_load(unsigned long *);`

`void ulong_store(unsigned long *, unsigned long *);`

`unsigned long ulong_get_and_set(unsigned long *, unsigned long );`

`void ulong_shift(unsigned long *, unsigned long *, unsigned long *);`

`_Bool ulong_compare_and_set(unsigned long *, unsigned long *, unsigned long);`

`unsigned long ulong_add_and_fetch(unsigned long *, unsigned long);`

`unsigned long ulong_sub_and_fetch(unsigned long *, unsigned long);`

`unsigned long ulong_and_and_fetch(unsigned long *, unsigned long);`

`unsigned long ulong_or_and_fetch(unsigned long *, unsigned long);`

`unsigned long ulong_xor_and_fetch(unsigned long *, unsigned long);`

`unsigned long ulong_nand_and_fetch(unsigned long *, unsigned long);`

`unsigned long ulong_fetch_and_add(unsigned long *, unsigned long);`

`unsigned long ulong_fetch_and_sub(unsigned long *, unsigned long);`

`unsigned long ulong_fetch_and_and(unsigned long *, unsigned long);`

`unsigned long ulong_fetch_and_or(unsigned long *, unsigned long);`

`unsigned long ulong_fetch_and_xor(unsigned long *, unsigned long);`

`unsigned long ulong_fetch_and_nand(unsigned long *, unsigned long);`

## size_t原子函数:

`void size_t_load(size_t *);`

`void size_t_store(size_t *, size_t *);`

`size_t size_t_get_and_set(size_t *, size_t);`

`void size_t_shift(size_t *v, size_t *, size_t *);`

`_Bool size_t_compare_and_set(size_t *, size_t *, size_t);`

`size_t size_t_add_and_fetch(size_t *, size_t);`

`size_t size_t_sub_and_fetch(size_t *, size_t);`

`size_t size_t_and_and_fetch(size_t *, size_t);`

`size_t size_t_or_and_fetch(size_t *, size_t);`

`size_t size_t_xor_and_fetch(size_t *, size_t);`

`size_t size_t_nand_and_fetch(size_t *, size_t);`

`size_t size_t_fetch_and_add(size_t *, size_t);`

`size_t size_t_fetch_and_sub(size_t *, size_t);`

`size_t size_t_fetch_and_and(size_t *, size_t);`

`size_t size_t_fetch_and_or(size_t *, size_t);`

`size_t size_t_fetch_and_xor(size_t *, size_t);`

`size_t size_t_fetch_and_nand(size_t *, size_t);`

## 有符号size_t（ssize_t）原子函数:

`void ssize_t_load(ssize_t *);`

`void ssize_t_store(ssize_t *, ssize_t *);`

`ssize_t ssize_t_get_and_set(ssize_t *, ssize_t);`

`void ssize_t_shift(ssize_t *, ssize_t *, ssize_t *);`

`_Bool ssize_t_compare_and_set(ssize_t *, ssize_t *, ssize_t);`

`ssize_t ssize_t_add_and_fetch(ssize_t *, ssize_t);`

`ssize_t ssize_t_sub_and_fetch(ssize_t *, ssize_t);`

`ssize_t ssize_t_and_and_fetch(ssize_t *, ssize_t);`

`ssize_t ssize_t_or_and_fetch(ssize_t *, ssize_t);`

`ssize_t ssize_t_xor_and_fetch(ssize_t *, ssize_t);`

`ssize_t ssize_t_nand_and_fetch(ssize_t *, ssize_t);`

`ssize_t ssize_t_fetch_and_add(ssize_t *, ssize_t);`

`ssize_t ssize_t_fetch_and_sub(ssize_t *, ssize_t);`

`ssize_t ssize_t_fetch_and_and(ssize_t *, ssize_t);`

`ssize_t ssize_t_fetch_and_or(ssize_t *, ssize_t);`

`ssize_t ssize_t_fetch_and_xor(ssize_t *, ssize_t);`

`ssize_t ssize_t_fetch_and_nand(ssize_t *, ssize_t);`

## 长长整型原子函数:

`void longlong_load(long long *);`

`void longlong_store(long long *, long long *);`

`long long longlong_get_and_set(long long *, long long);`

`void longlong_shift(long long *, long long *, long long *);`

`_Bool longlong_compare_and_set(long long *, long long *, long long);`

`long long longlong_add_and_fetch(long long *, long long);`

`long long longlong_sub_and_fetch(long long *, long long);`

`long long longlong_and_and_fetch(long long *, long long);`

`long long longlong_or_and_fetch(long long *, long long);`

`long long longlong_xor_and_fetch(long long *, long long);`

`long long longlong_nand_and_fetch(long long *, long long);`

`long long longlong_fetch_and_add(long long *, long long);`

`long long longlong_fetch_and_sub(long long *, long long);`

`long long longlong_fetch_and_and(long long *, long long);`

`long long longlong_fetch_and_or(long long *, long long);`

`long long longlong_fetch_and_xor(long long *, long long);`

`long long longlong_fetch_and_nand(long long *, long long);`

## 无符号长长整型原子函数:

`void ulonglong_load(unsigned long long *);`

`void ulonglong_store(unsigned long long *, unsigned long long *);`

`unsigned long long ulonglong_get_and_set(unsigned long long *, unsigned long long);`

`void ulonglong_shift(unsigned long long *, unsigned long long *, unsigned long long *);`

`_Bool ulonglong_compare_and_set(unsigned long long *, unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_add_and_fetch(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_sub_and_fetch(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_and_and_fetch(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_or_and_fetch(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_xor_and_fetch(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_nand_and_fetch(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_fetch_and_add(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_fetch_and_sub(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_fetch_and_and(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_fetch_and_or(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_fetch_and_xor(unsigned long long *, unsigned long long);`

`unsigned long long ulonglong_fetch_and_nand(unsigned long long *, unsigned long long);`

## 单精度符点数原子函数:

`void float_store(float *v, float *n);`

## 双精度符点数原子函数:

`void double_store(double *v, double *n);`

## 长双精度符点数原子函数:

`void longdouble_store(long double *v, long double *n);`