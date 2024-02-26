#将当前路径下的.c文件编译出对应的.o文件
OBJ=$(patsubst %.c, %.o, $(wildcard ./*.c))
#将编译生成的.o编译成指定的动态库
TARGET=libSoMyTree.so

$(TARGET):$(OBJ)
	$(CC) -shared -fPIC $^ -o $@
	
#将动态库放入/usr/lib/路径下
	cp $(TARGET) /usr/lib/
#模式匹配，将.c编译出对应的.o文件
%.o:%.c
	$(CC) -c $^ -o $@

clean:
	$(RM) $(OBJ) $(TARGET) 
	$(RM) /usr/lib/$(TARGET)