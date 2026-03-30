# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%Low Pass Filter Coefficient
n=0:1:N-1;
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))
%Blackman Window Sequence
n=0:1:N-1;
wh=0.42-0.5*cos((2*pi*n)/(N-1))+0.08*cos((4*pi*n)/(n-1))
hn=hd.*wh
% Plot the Low Pass Filter with Hanning Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'ms');
```
## OUTPUT:
<img width="1589" height="977" alt="image" src="https://github.com/user-attachments/assets/a340dc97-e7a5-46cd-959e-012c184df928" />

## RESULT:
![WhatsApp Image 2026-03-30 at 8 42 45 PM (2)](https://github.com/user-attachments/assets/02fc7328-b248-48f4-971f-8918de89216e)

