 # Analysis-of-open-loop-and-closed-loop-control-system
## Aim :
  To analyse the open loop and closed loop system having G(S)=1/(S^2+10S+20)  when an unit step input is applied using MATLAB.
## Apparatus Required:
  Computer with MATLAB software
## Theory
  ### Open loop control system
  In this system, the output doesn’t change the action of the control system. It doesn’t have any feedback. It is very simple, needs low maintenance, quick operation, and cost-effective. The accuracy of this system is low and less dependable.
  <img width="652" height="175" alt="image" src="https://github.com/user-attachments/assets/0a9d8129-eb64-40bb-8efd-434edcb2bd5a" />
 ### Closed loop control System
The closed-loop control system can be defined as the output of the system that depends on the input of the system. This control system has one or more feedback loops among its input & output. This system provides the required output by evaluating its input. This kind of system produces the error signal and it is the main disparity between the output and input of the system.
                     <img width="508" height="220" alt="image" src="https://github.com/user-attachments/assets/ad4b9b9e-bf06-4108-a4c0-5320be064b1f" />

Consider a system having plant G(S)=  1/(S^2+10S+20), H(S) = 1(negative unity feedback system) and Controller C(S) = 300.
C(S) and G(S) are in series, 300/(S^2+10S+20)
300/(S^2+10S+20) and H(S) are in negative feedback.
Therefore, Closed loop transfer function, (C(S))/(R(S))=300/(S^2+10S+320)
## Program: 
### Open loop System
```
num=[300];
den=[1 101 20]
sys=tf[num,den]
sys1=feedback(sys,1)
step(sys 1)
```

### Closed loop System
```
num=[300]
den=[1 10 320]
sys =tf(num,den)
t=0:0.01:2
step(sys,t)
```


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Analyse the result.
## Output:
### Open Loop System
![WhatsApp Image 2025-09-24 at 11 53 58_d6aa6eb5](https://github.com/user-attachments/assets/78384c65-886a-47a9-bab4-b9e89ae047fe)

### Closed Loop System
![WhatsApp Image 2025-09-24 at 11 53 31_dc71198a](https://github.com/user-attachments/assets/6178bb93-543e-430d-a0bd-1d5a8bf1dd86)

## Result:
Thus the open loop and closed loop system are analysed and the following conclusions are arrived.
### Open loop system
Steady State Error = 0.95
Settling Time = 2.01s
### Closed loop System
Steady State Error = 0.3
Settling Time = 0.186s





