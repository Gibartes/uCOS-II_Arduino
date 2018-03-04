

# MicroC/OS-II-Arduino

*********************************************************************************************************
#                                                uC/OS-II
#                                          The Real-Time Kernel


                              (c) Copyright 1992-2013, Micrium, Weston, FL
                                           All Rights Reserved

 
 By      : Jean J. Labrosse
 Version : V2.92.10

 LICENSING TERMS:
 ---------------
   uC/OS-II is provided in source form for FREE evaluation, for educational use or for peaceful research.
 If you plan on using  uC/OS-II  in a commercial product you need to contact Micrium to properly license
 its use in your product. We provide ALL the source code for your convenience and to help you experience
 uC/OS-II.   The fact that the  source is provided does  NOT  mean that you can use it without  paying a
 licensing fee.
*********************************************************************************************************

MicroC/OS for Arduino boards based on ARM Cortex M3 like Arudino Due.
This source code should be used just for education or research according to uC/OS-II's licensing terms.

Development stream storage : https://github.com/Gibartes/uCOS-II-Arduino.git

* OS_TASK_TMR_PRIO is defined as priority 15 in cfg/oscfg.h

2017.08.04
Revised by HongKyun, Gibartes

*********************************************************************************************************

# Usage

  Just include ucos_ii.h
  
  
  ......
  #include <ucos_ii.h>
    void setup(){
     ......
     
     OSInit();
     
     Create some tasks using OSTaskCreate(void (*task)(void *p_arg), void *p_arg, OS_STK *ptos, INT8U prio)
     
     OSTaskCreate(Task_Name,Task_Argument,Task_Stack_Pointer,Task_Priority);
     .....
    
     OSStart();
  }
