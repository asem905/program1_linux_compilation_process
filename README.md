used commands:
1-gcc -c task1.c
(same with task2 to get object file of each)
2-objdump -t task1.o
(to get symbol table)
3-gcc -static task1.c task2.c -o task.elf
(to get elf file using static linking)
4-readelf -s task.elf
(to get symbol table of resulting executable)
5-size task1.o | awk '{print"text size=",$1,"data size=",$2}'
(to read size of task1.o data and text segments)(same with task2.o and task.elf)
