# lab4

Part A：
--------------------
    0000000000601038 B __bss_start
    0000000000601038 b completed.6973
    0000000000601028 D __data_start
    0000000000601028 W data_start
    0000000000400430 t deregister_tm_clones
    00000000004004a0 t __do_global_dtors_aux
    0000000000600e18 t __do_global_dtors_aux_fini_array_entry
    0000000000601030 D __dso_handle
    0000000000600e28 d _DYNAMIC
    0000000000601038 D _edata
    0000000000601040 B _end
    00000000004005d4 T _fini
    00000000004004c0 t frame_dummy  
    0000000000600e10 t __frame_dummy_init_array_entry
    0000000000400768 r __FRAME_END__
    0000000000601000 d _GLOBAL_OFFSET_TABLE_
                     w __gmon_start__
    00000000004003a8 T _init
    0000000000600e18 t __init_array_end
    0000000000600e10 t __init_array_start
    00000000004005e0 R _IO_stdin_used
                     w _ITM_deregisterTMCloneTable
                     w _ITM_registerTMCloneTable
    0000000000600e20 d __JCR_END__
    0000000000600e20 d __JCR_LIST__
                     w _Jv_RegisterClasses
    00000000004005d0 T __libc_csu_fini
    0000000000400560 T __libc_csu_init
                     U __libc_start_main@@GLIBC_2.2.5
    0000000000400555 T main
    0000000000400460 t register_tm_clones
    0000000000400400 T _start
    0000000000601038 D __TMC_END__
    000000000040052d T average(int, float)
    00000000004004ed T average(double*, double&)
    
由上述結果可知，使用到的函數為average(int, float)和average(double*, double&)


Part B：
--------------------

Result：

    1 8
    4 8
    4 8
    8 8

Explanation：

    1 8  // size of char a, char *pa
    4 8  // size of int b, int *pb
    4 8  // size of float c, float *pc
    8 8  // size of double d, double *pd

From the course, we know the size of the fundamental variables:

character： 1 bytes

integer： 4 bytes

float： 4 bytes

double： 8 bytes

In addition, the pointer is loaded with the memory location. In a 64-bit operating system, a memory location occupies 8 bytes. So no matter what kind of pointer, its size is 8 bytes.
