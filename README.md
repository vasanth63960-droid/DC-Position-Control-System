# DC-Position-Control-System
## Aim:
To control the position of motor having the following specifications using MATLAB.<br>
(J)     moment of inertia of the rotor =    0.02 kg.m^2<br>
(b)     motor viscous friction constant =    0.002 N.m.s<br>
(Ktf)    motor torque constant   =           1.5 N.m/Amp<br>
(Ra)    armature resistance  =              2 Ohm<br>
(La)     armature inductance  =              0.5 H<br>
(Kb)      back emf constant = 0.5<br>
## Apparatus Required:
Computer with MATLAB software
## Theory: 
<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/acf6a293-6541-4891-b497-d3552b47f407" />
<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/d4f221d1-a9d4-4e37-8e63-0caf31769ef6" />
<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/96071858-75b1-4582-805e-ed5953dc40de" />
<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/559c913f-801a-4faf-a6de-d4db09adcc2b" />



## Procedure:
1.	Open MATLAB software
2.	Open a new script file.
3.	Type the program.
4.	Save and Execute the program.
5.	Analyse the output in open loop and closed loop.

## Program
Kt = 1.5;
J = 0.02;
B = 0.002;
Ra = 2;
La = 0.5;
Kb = 0.5;
S = tf('s');
ol_sys = Kt / ((J*S*S+B*S)*(Ra+La*S)+Kt*Kb*S);
subplot(2,1,1)
step(ol_sys)
title('Open-Loop Step Response');
Cl_sys = feedback(1*ol_sys,1);
subplot(2,1,2)
step(Cl_sys)
title('Closed-Loop Step Response');
## Output
<img width="668" height="521" alt="image" src="https://github.com/user-attachments/assets/77179d1b-8a5a-4875-9870-df9b184f7bfe" />
<img width="525" height="428" alt="image" src="https://github.com/user-attachments/assets/8fbaddd4-e566-40df-8646-1184143789c1" />


## Result
Thus, the position of dc motor is controlled using MATLAB. 
