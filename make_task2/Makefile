# 'clean' added to avoid 'up to date' status after make clean
# because added empty 'clean' file

.PHONY: all clean

all: inc_1 inc_2 inc_3 task_2

task_2: main.o src1.o src2.o src3.o
	gcc $^ -o $@

inc_1:
ifeq ($(METHOD),1)
	make -f make1.mk
else ifeq ($(METHOD),2)
include make1.mk
else
	@echo "Error!. Specify METHOD variable. Example: make METHOD=1 - for 'make -f', '2' for include.\n"
	exit 1
endif

inc_2:
ifeq ($(METHOD), 1)
	make -f make2.mk
else ifeq ($(METHOD), 2)
include make2.mk
else
	@echo "Error!. Specify METHOD variable. Example: make METHOD=1 - for 'make -f', '2' for include.\n"
	exit 1
endif

inc_3:
ifeq ($(METHOD), 1)
	make -f make3.mk
else ifeq ($(METHOD), 2)
include make3.mk
else
	@echo "Error!. Specify METHOD variable. Example: make METHOD=1 - for 'make -f', '2' for include.\n"
	exit 1
endif

main.o: main.c
	gcc -c $< -o $@

clean:
	rm -f ./*.o ./task_2