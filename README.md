# GUI-Assignment-1
operator control panel

%Clear workspace area and command
clc;
clear;
%Closes any existing graphs
close all;
format compact

%Set variable
L1 = 1250;
theta1 = 35; %In degrees

%Set variable
L2 = 1250;
theta2 = 45; %In degrees

%Creating for loop
for theta = 0:5:180
    
    theta= deg2rad(theta);
    
   %Calculate first joint position
x1 = L1*cos(theta1);
y1 = L1*sin(theta1);

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

end

end
