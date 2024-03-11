1
% Problem 1: Convert polar coordinates to rectangular coordinates

% Define polar coordinates
r = 5; % radius
theta = pi/4; % angle in radians

% Convert polar coordinates to rectangular coordinates
x = r * cos(theta);
y = r * sin(theta);

% Display the results
fprintf('Rectangular coordinates:\n');
fprintf('x = %.2f\n', x);
fprintf('y = %.2f\n', y);

3

% Define the radius of the tank
r = 10; % for example, you can change this value as needed

% Calculate the cost C using the formula
C = (32430 / r) + 428;

% Display the result
fprintf('The cost of the containment tank with radius %.2f is $%.2f\n', r, C);

7

% Define the coefficient matrix A and the constant matrix B
A = [6, -4, 8; -5, -3, 7; 14, 9, -5];
B = [112; 75; -67];

% Solve for x
x = A \ B;

% Display the solution
fprintf('Solution:\n');
fprintf('x = %.2f\n', x(1));
fprintf('y = %.2f\n', x(2));
fprintf('z = %.2f\n', x(3));

8
% This script calculates the volume of a hollow sphere
% Define the inner and outer radii of the hollow sphere
r_inner = 5; % Inner radius, you can change this value as needed
r_outer = 7; % Outer radius, you can change this value as needed
% Calculate the volume of the hollow sphere
volume = (4/3) * pi * (r_outer^3 - r_inner^3);
% Display the result
fprintf('The volume of the hollow sphere is %.2f cubic units\n', volume);

9

% Define variables
r_inner = 10; % Inner radius
thickness = 2; % Thickness
r_outer = r_inner + thickness; % Calculate outer radius

% Calculate volume of hollow sphere
volume = (4/3) * pi * ((r_outer)^3 - (r_inner)^3);

% Display output
fprintf('The volume of the hollow sphere is: %.2f\n', volume);

10
function thirdside()
    fprintf('>> thirdside\n\n');

    % Prompt user for input
    b = input('Enter the first side: ');
    c = input('Enter the second side: ');
    angle_degrees = input('Enter the angle between them: ');

    % Calculate the third side
    third_side = calculate_third_side(b, c, angle_degrees);

    % Print the result
    fprintf('The third side is %.3f\n', third_side);
end

function third_side = calculate_third_side(b, c, angle_degrees)
    angle_radians = deg2rad(angle_degrees);
    a_squared = b^2 + c^2 - 2*b*c*cos(angle_radians);
    third_side = sqrt(a_squared);
end

11
% Define altitudes and corresponding temperatures
altitudes = [1000; 2000; 3000; 4000; 5000]; % Altitudes in meters
temperatures = [288; 281; 269; 254; 249]; % Temperatures in Kelvin
% Combine altitudes and temperatures into a table
table_data = [altitudes, temperatures];
% Display the table
disp('Altitude (m)    Temperature (K)');
disp(table_data);

13

% Define the range of t
t = linspace(0, 2*pi, 100); % 100 points between 0 and 2*pi

% Calculate y1, y2, y3, and y4
y1 = sin(t);
y2 = cos(t);
y3 = y1.^2;
y4 = y2.^2;

% Create subplots
subplot(2, 2, 1);
plot(t, y1, 'b', 'LineWidth', 2);
xlabel('t');
ylabel('y_1 = sin(t)');
title('Plot of y_1');

subplot(2, 2, 2);
plot(t, y2, 'r', 'LineWidth', 2);
xlabel('t');
ylabel('y_2 = cos(t)');
title('Plot of y_2');

subplot(2, 2, 3);
plot(t, y3, 'g', 'LineWidth', 2);
xlabel('t');
ylabel('y_3 = y_1^2');
title('Plot of y_3');

subplot(2, 2, 4);
plot(t, y4, 'm', 'LineWidth', 2);
xlabel('t');
ylabel('y_4 = y_2^2');
title('Plot of y_4');

14

% Define the values
yr = [1988, 1994];
sle = [8, 12, 20, 22, 18, 24, 27];
% Create the bar plot
bar(yr, sle);
% Add labels for x-axis and y-axis
xlabel('Year');
ylabel('SLE (mm)');
% Add title
title('SLE (Sea Level Elevation) for Years 1988 and 1994');
% Adjust the appearance
grid on;
% Show plot

15

% Define theta values
theta = linspace(0, 2*pi, 1000);
% Calculate corresponding r values
r = 3*cos(0.5*theta).^2 + theta;
% Plot polar plot
polarplot(theta, r);
title('r = 3cos^2(0.5\theta) + \theta');

12

% Define the range of x1 and x2
x1 = linspace(0, 40, 100); % 100 points between 0 and 40
x2 = linspace(0, 20, 100); % 100 points between 0 and 20

% Calculate y1 and y2
y1 = 4 * cos(x1) ./ (x1 + 2);
y2 = x2.^2 ./ x2.^3;

% Plot y1
figure;
plot(x1, y1, 'b', 'LineWidth', 2);
hold on;

% Plot y2
plot(x2, y2, 'r--', 'LineWidth', 2);

% Add labels and legend
xlabel('x');
ylabel('y');
legend('y_1 = 4cos(x_1) / (x_1 + 2)', 'y_2 = x_2^2 / x_2^3', 'Location', 'northwest');
title('Plot of y_1 and y_2');

% Adjust the axis limits for better visualization
axis([0 40 -2 2]);

% Show grid
grid on;

% Show plot
hold off;

