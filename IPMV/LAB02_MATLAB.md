# Code
```
clc;
close all;
clear all;
figure(1);
I1 = imread('test1.jfif');
imshow(I1);
pause
I1g = rgb2gray(I1);
figure;
imshow(I1g);
pause
I1gn = 255 -I1g;
figure;
imshow(I1gn);
pause
c=3;
I1g2 = im2double(I1g);
I2t = c*log10(1+ I1g2);
figure;
imshow(I2t);
pause
% thresholding logic
threshold = 120;
Ithres = I1g;
Ithres(Ithres <= threshold) = 0;
Ithres(Ithres > threshold) = 255;
figure;
imshow(Ithres);
% bitscaling
A=I1g;
B=bitget(A,1); subplot(3,3,1), imshow(logical(B));title('Bit plane 1');
B=bitget(A,2); subplot(3,3,2), imshow(logical(B));title('Bit plane 2');
B=bitget(A,3); subplot(3,3,3), imshow(logical(B));title('Bit plane 3');
B=bitget(A,4); subplot(3,3,4), imshow(logical(B));title('Bit plane 4');
B=bitget(A,5); subplot(3,3,5), imshow(logical(B));title('Bit plane 5');
B=bitget(A,6); subplot(3,3,6), imshow(logical(B));title('Bit plane 6');
B=bitget(A,7); subplot(3,3,7), imshow(logical(B));title('Bit plane 7');
B=bitget(A,8); subplot(3,3,8), imshow(logical(B));title('Bit plane 8');

```
