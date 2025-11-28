# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
<img width="520" height="715" alt="image" src="https://github.com/user-attachments/assets/c5cc36c5-dab4-4bf3-a715-ab56260a83a6" />
<img width="594" height="794" alt="image" src="https://github.com/user-attachments/assets/9993b27d-f4a0-4132-ba86-ff84797440a3" />




## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1

den=[0.05 0.6 1 0]

sys=tf(num,den)

bode(sys)

grid on

[Gm Pm Wpc Wgc]=margin(sys)

if(Wpc>Wgc)

    disp('stable')
elseif(Wpc == Wgc)

    disp('marginally stable')
else

    disp('unstable')
end
```
## Output:
<img width="695" height="521" alt="Screenshot 2025-11-17 114652" src="https://github.com/user-attachments/assets/b8589a02-bcb9-489e-942f-6b32d587fb6d" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12.0000
Phase Margin =60.4231
Gain crossover frequency =  0.9070
Phase crossover frequency = 4.4721
The system is STABLE
