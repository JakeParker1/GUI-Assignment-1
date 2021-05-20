# GUI-Assignment-1
operator control panel


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
plot(a,b,"MarkerSize",15);

%Keep last plot on
hold on;

%Create a rectangle to represent the DCIC
%Set Variables
x = [-2000 2000 2000 -2000 -2000];
y = [0 0 3000 3000 0];

%Plotting the rectangle
plot(x,y);

%Turn grid lines on
grid on

end

end
