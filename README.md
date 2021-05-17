# GUI-Assignment-1
operator control panel

%Clear inputs from workspace area
clear
%Clear text from comand window
clc
%Closes functions
close all

%Set variable
L1 = 1250;
theta1 = 30; %In degrees

%Calculate first joint position
x1 = L1*cosd(theta1);
y1 = L1*sind(theta1);

%Set variable
L2 = 1250;
theta2 = 30; %In degrees

%Calculate second joint position
x2 = x1+L2*cosd(theta1+theta2);
y2 = y1+L2*sind(theta1+theta2);

%Plot first position with a o at size 10
plot(x1,y1,'-o','MarkerSize',10)

%Label axis from 0 to 2000 on x axis and -3000 to 0 on y axis
axis([0 2000 -3000 0])

hold on;

%Plot second position with an x at size 10
plot(x2,y2,'-x','MarkerSize',10)

%Grid references added
grid on;
