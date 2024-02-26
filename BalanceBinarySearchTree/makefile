#自定义变量
#变量赋值
OBJ=$(patsubst %.c,%.o,$(wildcard ./*.c))
TARGET=main

LDFLAGS=-L./src_so
LIBS=-lSoMyTree 

#使用$(TARGET)，必须要加$符号
$(TARGET):$(OBJ)
	$(CC) $^ $(LIBS) $(LDFLAGS) -o $@

%.o:%.c
	$(CC) -c $^ -o $@

.PHONY: clean

clean:
	@$(RM) *.o $(TARGET)

show:
	@echo $(RM)
	@echo $(CC)
	@echo $(CXX)
	@echo $(wildcard ./*.c)
	@echo $(patsubst %.c,%.o,$(wildcard ./*.c))