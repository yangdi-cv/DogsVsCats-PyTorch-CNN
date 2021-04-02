# DogsVsCats
Algorithm competition organized by Kaggle, used for PyTorch initial study

## Dataset
Provided from Microsoft Research: https://www.kaggle.com/c/dogs-vs-cats/data

## Convolutional network design
![CNN](https://github.com/Ericdiii/DogsVsCats-PyTorch-CNN/blob/main/CNN.png)
1. **Input**: Adjust image to `200×200` pixels
2. **ConV1**: The scale of convolutional core is `(3×3×3×16)`, hight=`3`, width=`3`, #layer=`3`, #filters=`16`
3. **Result of first convolution**: `(200×200×16)` feature map
4. **Pooling**: `2×2` Max pooling
5. **Result of first pooling**: The image is reduced to `100×100` pixels
6. **ConV2**: The scale of convolutional core is `(3×3×16×16)`, hight=`3`, width=`3`, #layer=`16`, #filters=`16`
7. **Result of second convolution**: `(100×100×16)` feature map
8. **Pooling**: `2×2` Max pooling
9. **Result of second pooling**: The image is reduced to `50×50` pixels
10. **FC1**: First full connected layer, 50×50×16=`40000` input nodes, `128` output nodes, output data is `(128×1)`
11. **FC2**: Second full connected layer, `128` input nodes, `64` output nodes, output data is `(64×1)`
12. **FC3**: Third full connected layer, `64` input nodes, `2` output nodes to represent the percentage of cat or dog (Using Softmax method to transform)

## Run

1. Set data directory
2. **RUN** train.py
3. **RUN** test.py

## Source
(https://github.com/xbliuHNU)https://github.com/xbliuHNU/DogsVsCats
Authur [@xbliuHNU]