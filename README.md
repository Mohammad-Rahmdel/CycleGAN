## CycleGAN - Tensorflow 2
[Paper: Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks](https://arxiv.org/abs/1704.00028)


The goal is to learn mapping functions between two domains X and Y given training samples. Training samples are from unpaired datasets. In such datasets there is no information provided as to which image from input domain(X) matches which image in output domain(Y). However, we assume there is some underlying relationship between the domains – for example, that they are
two different renderings of the same underlying scene – and
seek to learn that relationship.

Objective function contains two types of terms: adversarial losses (GAN Loss) for matching the distribution of generated images to the data distribution in the target domain; and cycle consistency losses to prevent the learned mappings G and F from contradicting each other. G refers to the generator which maps X to Y and F does the vice-versa.


## Tensorflow2 Implementation 

[Here](https://github.com/Mohammad-Rahmdel/CycleGAN/tree/master/CycleGAN.ipynb) is the implementation of CycleGAN paper. It is implemented in Google Colab. If you want to run it on your system you should make some changes!

Set your desired resolution of images. Also select the dataset you want. You can find the dataset choices [here](https://people.eecs.berkeley.edu/%7Etaesung_park/CycleGAN/datasets/).


<table align='center'>
 <tr align='center'>
<td> Epoch 1 </td>
<td> Epoch 100 </td>
</tr>
<tr align='center'>
<td> <img src = 'results/apple2orange/e1.png'>
<td> <img src = 'results/apple2orange/e100.png'>
</tr>
</table>


<table align='center'>
 <tr align='center'>
<td> Epoch 1 </td>
<td> Epoch 100 </td>
</tr>
<tr align='center'>
<td> <img src = 'results/apple2orange/Y2X-1.png'>
<td> <img src = 'results/apple2orange/Y2X-108.png'>
</tr>
</table>


I used four different datasets to train the networks.

### Results ### 

I trained the model on four different unpaired datasets.


#### monet2photo
Number of trained epochs: 60  <br>
Resoltion: 256*256  <br>

Results on dataset samples: <br>


<p align="center">
    photo to monet
</p>
<table align='center'>	
<tr align='center'>
<td> <img src = 'results/monet2photo/dataset_samples/1.png'>
<td> <img src = 'results/monet2photo/dataset_samples/3.png'>
</tr>	
<tr align='center'>
<td> <img src = 'results/monet2photo/dataset_samples/4.png'>
<td> <img src = 'results/monet2photo/dataset_samples/6.png'>
</tr>
</table>

Results on random samples(These images are not given to the model in training time) <br>


<p align="center">
    photo to monet
</p>
<table align='center'>	
<tr align='center'>
<td> <img src = 'results/monet2photo/my_images/1.png'>
<td> <img src = 'results/monet2photo/my_images/4.png'>
</tr>	
<tr align='center'>
<td> <img src = 'results/monet2photo/my_images/5.png'>
<td> <img src = 'results/monet2photo/my_images/6.png'>
</tr>
<tr align='center'>
<td> <img src = 'results/monet2photo/my_images/7.png'>
<td> <img src = 'results/monet2photo/my_images/8.png'>
</tr>
<tr align='center'>
<td> <img src = 'results/monet2photo/my_images/9.png'>
<td> <img src = 'results/monet2photo/my_images/10.png'>
</tr>
</table>



#### vangogh2photo
Number of trained epochs: 200  <br>
Resoltion: 256*256  <br>


dataset samples <br>
<p align="center">
    photo to vangogh
</p>
<img src='./results/vangogh2photo/dataset_samples/photo2vanghogh3.png' />​​ <br>
<img src='./results/vangogh2photo/dataset_samples/photo2vanghogh4.png' />​​ <br>
<img src='./results/vangogh2photo/dataset_samples/photo2vanghogh5.png' />​​ <br>


random samples <br>

<p align="center">
    photo to vangogh
</p>
<table align='center'>	
<tr align='center'>
<td> <img src = 'results/vangogh2photo/my_images/v1.png'>
<td> <img src = 'results/vangogh2photo/my_images/v2.png'>
</tr>	
<tr align='center'>
<td> <img src = 'results/vangogh2photo/my_images/v3.png'>
<td> <img src = 'results/vangogh2photo/my_images/v4.png'>
</tr>	
<tr align='center'>
<td> <img src = 'results/vangogh2photo/my_images/v5.png'>
<td> <img src = 'results/vangogh2photo/my_images/v6.png'>
</tr>	
</table>




#### apple2orange
Number of trained epochs: 200 <br>
Resoltion: 128*128 <br>


<p align="center">
    apple to orange
</p>
<table align='center'>
<tr align='center'>
<td> <img src = 'results/apple2orange/2.png'>
<td> <img src = 'results/apple2orange/3.png'>
</tr>
<p align="center">
    orange to apple
</p>
<tr align='center'>
<td> <img src = 'results/apple2orange/10.png'>
<td> <img src = 'results/apple2orange/11.png'>
</tr>
</table>



<table align='center'>
<tr align='center'>
<td> input image </td>
<td> predicted image </td>
<td> cycled image </td>
</tr>
<tr align='center'>
<td> <img src = 'results/apple2orange/12.png'>
</tr>
<tr align='center'>
<td> <img src = 'results/apple2orange/13.png'>
</tr>
</table>



#### horse2zebra
Number of trained epochs: 200  <br>
Resoltion: 128*128  <br>

<img src='./results/horse2zebra/X2Y-100.png' />​​ <br>


<table align='center'>
<tr align='center'>
<td> input image </td>
<td> predicted image </td>
<td> cycled image </td>
</tr>
<tr align='center'>
<td> <img src = 'results/horse2zebra/index.png'>
</tr>
</table>




You can find more generated samples [here](https://github.com/Mohammad-Rahmdel/CycleGAN/tree/master/results).



