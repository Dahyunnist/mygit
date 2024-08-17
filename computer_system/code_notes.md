2024-08-08
1. 指针与数组
   - 可以先定义指针指向的类型，即定义了数组元素的类型，然后通过给指针分配内存来创建数组。
    ``` 
        ElementType *p;
        p = (ElementType*)malloc(sizeof(ElementType) * arraySize);
      ```
      这样就创建了一个长度为arraySize的数组，其中每个元素的类型为ElementType。
    