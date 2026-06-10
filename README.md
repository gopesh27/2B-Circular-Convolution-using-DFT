# EXPT 2B:CIRCULAR-CONVOLUTION-USING-DFT
## AIM
To perform and verify circular convolution operation of two given sequences using SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM:
## CIRCULAR CONVOLUTION
~~~
clc; clear; 
x=[1 1 1 1]; 
n1=0:1:length(x)-1; 
subplot(3,1,1); 
plot2d3(n1,x); 
xlabel('time'); 
ylabel('amplitude'); 
title('input sequence'); 
h=[1 2 3]; 
n2=0:1:length(h)-1; 
subplot(3,1,2); 
plot2d3(n2,h); 
xlabel('time'); 
ylabel('amplitude'); 
title('impulse sequence'); 
N1=length(x); 
N2=length(h); 
N=max(N1,N2); 
N3=N1-N2; 
if(N3>0) 
h=[h,zeros(1,N3)]; 
else 
x=[x,zeros(1,abs(N3))]; 
end 
disp(x) 
disp(h) 
for n=1:N 
y(n)=0; 
for i=1:N 
j=n-i+1; 
if(j<=0) 
end 
j=N+j; 
y(n)=y(n)+x(i)*h(j); 
end 
end 
disp(y) 
n=0:N-1; 
subplot(3,1,3); 
plot2d3(n,y); 
xlabel('time'); 
ylabel('amplitude'); 
title('circular convolution');
~~~
<br>
<br>
<br>
<br>
<br>

<br>
### CALCULATIONS:
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/d6c6ef7b-5e2a-4c3a-87e2-99652c00be9b" />
<img width="1599" height="899" alt="image" src="https://github.com/user-attachments/assets/5d5ae839-5955-4c8b-a3e4-fab9c5bd1351" />

<br>
<br>
<br>
<br>
<br>
### SAMPLE OUTPUT:
<img width="900" height="178" alt="image" src="https://github.com/user-attachments/assets/a4d3a29a-fd2b-4090-86dc-87e5545855f9" />

<br>
<br>
<br>
<br>



## RESULT:
Thus, the circular convolution of the two given sequences were performed and its result was verified.
