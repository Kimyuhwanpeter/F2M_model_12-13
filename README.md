# F2M_model_12-13

## F2M_model_12 (GPU 메모리 제안, filter 크기를 각각 반으로 줄이고 학습중)
* Depth wise + point wise (Depth-wise Separable Convolution, Xception model에 사용했던 기법)을 Residual block (Dilated rate 한 블록을 거칠때마다 2씩 증가.)에 적용(채널에 대한 정보 + spatial space 정보를 각각 분리한것). Attention 추가 (gradient image를 구한 후 sigmoid 처리). 1x1 Depth wise conv encoder 단에 추가. Decoder에 reverse residual block (Dilated rate 한 블록을 거칠때마다 4씩 증가.) 추가. 각 block에 있는 1x1 depth wise conv 를 1x1 conv 로 변경. Encoder에 있는 각각의 conv layer에 attention 추가(gradient image 후 sigmoid)
![f5](https://github.com/Kimyuhwanpeter/F2M_model_12-13/blob/main/f5.png)
<br/>

## F2M_model_13 (GPU 메모리 제안, filter 크기를 각각 반으로 줄이고 학습중)
* model_12에서 decoder의 dilate를 8로 증가하고 1번 반복으로 바꿈
![f6](https://github.com/Kimyuhwanpeter/F2M_model_12-13/blob/main/f6.png)
