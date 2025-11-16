# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
<img width="965" height="1600" alt="image" src="https://github.com/user-attachments/assets/191956bf-0692-4eeb-a5bc-6059b34faece" />
<img width="1573" height="1600" alt="image" src="https://github.com/user-attachments/assets/6965f26b-72f5-45e0-8a0c-6912d2d2fa34" />


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=[1];
den=[0.05 0.6 1 0];
sys=tf(num,den)
bode(sys)
grid on;
[gm pm wpc wgc]=margin(sys)
gmindb=20*log10(gm)
if(wpc>wgc)
    disp('stable')
elseif(wpc==wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```

## Output:
<img width="1920" height="1080" alt="CS EXP5" src="https://github.com/user-attachments/assets/a0f60270-4bf9-4fe6-8ea9-1d6efffa2fb2" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin =40DB <br>
Phase Margin =70DEGREE <br>
Gain crossover frequency =1 rad/s <br>
Phase crossover frequency =20 rad/s <br>
The system is STABLE ------------
