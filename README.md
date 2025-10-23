# EXPERIMENT--02-INTEFACING-A-DIGITAL-INPUT-TO-ARM-DEVELOPMENT-BOARD
## Aim: To Interface a Digital Input  (userpush button  ) to ARM   development board and write a  program to obtain  the data and flash the led 
## NAME: PRAVISH J
## REF NO: 212224040249

7.click on cntrl+S , automaticall C program will be generated 
![image](https://user-images.githubusercontent.com/36288975/226189443-8b43451d-0b14-47e4-a20b-cc09c6ad8458.png)
![image](https://user-images.githubusercontent.com/36288975/226189450-85ffa969-2ffb-4788-81e5-72d60fdda0f1.png)
8. edit the program and as per required 
![image](https://user-images.githubusercontent.com/36288975/226189461-a573e62f-a109-4631-a250-a20925758fe0.png)

9. use project and build all 
![image](https://user-images.githubusercontent.com/36288975/226189554-3f7101ac-3f41-48fc-abc7-480bd6218dec.png)
10. once the project is bulild 
![image](https://user-images.githubusercontent.com/36288975/226189577-c61cc1eb-3990-4968-8aa6-aefffc766b70.png)

11. click on debug option 
![image](https://user-images.githubusercontent.com/36288975/226189625-37daa9a3-62e9-42b5-a5ce-2ac63345905b.png)

12. connect the  ARM board to power supply and usb 


13. check for execution of the output using run option 



## STM 32 CUBE PROGRAM :
```C
#include "main.h"
#include "stdbool.h"
void push_button();
bool button_status;

void push_button(){
	button_status=HAL_GPIO_ReadPin(GPIOA,GPIO_PIN_0);
	if(button_status==0)
	{
		HAL_GPIO_WritePin(GPIOB,GPIO_PIN_0,GPIO_PIN_SET);
		HAL_Delay(500);
		HAL_GPIO_WritePin(GPIOB,GPIO_PIN_0,GPIO_PIN_RESET);
		HAL_Delay(500);
	}
	else{
		HAL_GPIO_WritePin(GPIOB,GPIO_PIN_0,GPIO_PIN_RESET);
		HAL_Delay(500);
	}
}

  while (1)
  {
	  push_button();
  }
```


## Output  :
 ![Screenshot 2024-08-29 184617](https://github.com/user-attachments/assets/1ff9a79e-58c2-4e5a-8d31-99d678bde8d8)

## Layout of the circuit :
![Screenshot 2024-08-29 184748](https://github.com/user-attachments/assets/bb0244e0-85ce-46ae-b637-9e016a6b6e76)

 
 
## Result :
Interfacing a digital Input (Pushbutton ) with ARM microcontroller based IOT development is executed and the results are verified.
