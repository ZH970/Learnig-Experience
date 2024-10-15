# ***Build A New Project on Keil MDK***



1. 建立工程文件夹，keil新建并选择芯片型号
2. 工程文件夹里建立Start、Library、User等文件夹 复制固件库里面的文件到工程文件夹
3. keil内添加对应文件到Start、Library、User 新建分组里
4. 工程选项c/c++ include Paths 生命所有包含头文件的文件夹
5. _并且define 内定义USE_STDPERIPH_DRIVER标准库_
6. debug 下拉列表选择对应调试器

# ***GPIO USAGE***

1. `RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA,ENABLE);` 启用GPIO口的时序，Ax 就是GPIOA，Cx就是GPIOC

2. 

`GPIO_InitTypeDef GPIO_InitStructure; ` 声明结构体

`GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP; ` 规定工作模式为推挽输出（模拟输入(AIN)、浮空输入(IN_FLOATING)、下拉输入(IPD)、上拉输入 (IPU)、开漏输出(Out OD)、推挽输出(Out PP)

`GPIO_InitStructure.GPIO_Pin = GPIO_Pin_5(|GPIO_Pin_x);` 设置管脚

`GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;` GPIO 管脚速度

初始化

3. `GPIO_ResetBits(GPIOC,GPIO_Pin_13);` // Set 0 flash on PC13
4. `GPIO_WriteBit(GPIOA,GPIO_Pin_5,Bit_RESET);` // Set 0 flash on A5
5. 
