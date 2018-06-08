# Barcode detect, decode using DL

## Some good posts

[Decoding 1-D Barcode from Degraded Images Using a Neural Network](http://what-when-how.com/computer-visionimaging-and-computer-graphics/decoding-1-d-barcode-from-degraded-images-using-a-neural-network-computer-visionimaging-and-computer-graphics-part-1/)


The existing open-source libraries for 1-D barcodes recognition are not able to recognize the codes 
from images acquired using simple devices without autofocus or macro function

ZXing project : best open-source barcode decoed, but still need need autofocus and high resolution

This papaer : use image restoration technique to improve accuracy of Barcode decoder

流れの概要

1. Image restoration
2. Barcodes Decoding
2.1 Identification
2.2 Decoding

[Reading barcodes with
neural networks](https://pdfs.semanticscholar.org/380a/e14aa6f260ee85cc062da6631e84d6ee68cd.pdf)

流れの概要

1. PyBarを用いて、Barcode画像生成する
2. 生成された画像をAugmenting techniqueで学習データ生成
.....
