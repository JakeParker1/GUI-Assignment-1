# GUI-Assignment-1
operator control panel

%SCARA Robot positions with large waste

%Clear workspace area and command
clc;
clear;
%Closes any existing graphs
close all;
format compact

%Set variable
L1 = 1300;
theta1 = 35; %In degrees

%Set variable
L2 = 1400;
theta2 = 45; %In degrees

%Creating for loop
for theta = 0:5:180
    
    theta = deg2rad(theta);
    
   %Calculate first joint position
x1 = L1*cos(theta);
y1 = L1*sin(theta);

%Creating for loop
for theta2 = 0:5:120
    
       theta2 = theta + deg2rad(theta2);
    
    %Calculate second joint position
x2 = x1+L2*cos(theta2);
y2 = y1+L2*sin(theta2);


%Plot first position with a o at size 10
plot(x1,y1,'-o','MarkerSize',10)

%Label axis from 0 to 2000 on x axis and -3000 to 0 on y axis
axis([-3500 3500 0 3000])

%Keep last plot on
hold on;

%Plot second position with an x at size 10
plot(x2,y2,'-x','MarkerSize',10)

%Keep last plot on
hold on;

%Create a circle to represent DCIC
%Set variables
x = 0;
y = 1500;
r = 1000;

%Operating limits of the circle 
th = 0:pi/100:2*pi;

%Working out angles of the circle
a = r*cos(th) + x;
b = r*sin(th) + y;

%Plot the circle
plot(a,b,"LineWidth",3);

%Keep last plot on
hold on;

%Create 1st rectangle to represent the DCIC
%Set Variables
x = [-2000 2000 2000 -2000 -2000];
y = [0 0 3000 3000 0];

%Plotting the 1st rectangle
plot(x,y,"LineWidth",3);

%Create 2nd rectangle to represent small waste
%Set variables
x = [-2000 -1300 -1300 -2000 -2000]
y = [0 0 900 900 0];

%Plotting 2nd rectangle
plot(x,y,"LineWidth",3);

%Create 3rd rectangle to represent small waste
%Set variables
x = [1300 2000 2000 1300 1300];
y = [0 0 900 900 0];

%Plotting 3rd rectangle
plot(x,y,"LineWidth",3);

%Create 4th rectangle to represent small waste
%Set Variables
x = [-2000 -1300 -1300 -2000 -2000];
y = [2100 2100 3000 3000 2100];

%Plotting 4th rectangle
plot(x,y,"LineWidth",3);

%Create 5th rectangle to represent small waste
%Set variables
x = [1300 2000 2000 1300 1300];
y = [2100 2100 3000 3000 2100];

%Plotting 5th rectangle
plot(x,y,"LineWidth",3);

%Turn grid lines on
grid on

end

end
