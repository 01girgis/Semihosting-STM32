# Semihosting in STM32 (STM32CubeIDE)


## #1 : In Project Properties, select C/C++ Build, then Settings , then Add to Miscellaneous 
```
-specs=rdimon.specs -lc -lrdimon
```
photo

## #2 : Exclude syscall.c file by clicking  Right Click , then  Resource Configuration , select exclude from build  

photo

## #3 : Select Debug & Release  , then OK


photo

## #4 : Add Function Prototype out of the main Function 

```c
extern void initialise_monitor_handles(void);
```

photo


## #5 : Add The Following Function Call inside main. 

```c
initialise_monitor_handles();
```

photo

## #6 : In Debug Configurations select Startup Tab , the Add This Configuration Line .

```c
monitor arm semihosting enable
```
photo
photo

