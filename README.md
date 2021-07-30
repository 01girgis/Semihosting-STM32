# Semihosting in STM32 (STM32CubeIDE)


## #1 : In Project Properties, select C/C++ Build, then Settings , then Add to Miscellaneous 
```
-specs=rdimon.specs -lc -lrdimon
```
<p align="center">
<img src="samples/1.png"  width="400" height="400" />
</p>


## #2 : Exclude syscall.c file by clicking  Right Click , then  Resource Configuration , select exclude from build  

<p align="center">
<img src="samples/3.png"  width="400" height="400" />
</p>

## #3 : Select Debug & Release  , then OK


<p align="center">
<img src="samples/4.png"  width="400" height="400" />
</p>

## #4 : Add Function Prototype out of the main Function 

```c
extern void initialise_monitor_handles(void);
```

<p align="center">
<img src="samples/5.png"  width="400" height="400" />
</p>


## #5 : Add The Following Function Call inside main. 

```c
initialise_monitor_handles();
```

<p align="center">
<img src="samples/6.png"  width="400" height="400" />
</p>

## #6 : In Debug Configurations select Startup Tab , the Add This Configuration Line .

```c
monitor arm semihosting enable
```

<p align="center">
<img src="samples/7.png"  width="400" height="400" />
</p>

<p align="center">
<img src="samples/8.png"  width="400" height="400" />
</p>
