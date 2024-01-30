# PhysicsLab2
clc;
clear all;
%Inputs
V1 = input("Input for vector 1: ");
V2 = input("Input for vector 2: ");
V3 = input("Input for vector 3: ");

VT = V1 + V2 + V3;
%Drawing
figure;

quiver(0, 0, V1(1), V1(2), 0, 'Color', 'red', 'DisplayName', 'Vector 1');

hold on;

quiver(V1(1), V1(2), V2(1), V2(2), 0);

hold on;

quiver((V2(1)+V1(1)), (V2(2)+V1(2)), V3(1), V3(2), 0);

hold on;

quiver(0, 0, VT(1), VT(2), 0);

hold on;
%Set the limits
%Both were changed to -5,5 for the last figure
xlim([-2,2]);
ylim([-2,2]);
%Label
xlabel('X-axis');
ylabel('Y-axis');
title('Vector addition');
