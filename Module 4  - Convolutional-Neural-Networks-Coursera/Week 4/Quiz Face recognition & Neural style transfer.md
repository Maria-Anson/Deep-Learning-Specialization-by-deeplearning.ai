> ## Special applications: Face recognition & Neural style transfer
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> Face verification requires comparing a new picture against one person’s face, whereas face recognition requires comparing a new picture against K person’s faces. 
> 
> Check
>
     True
> Correct
> 
> 1 / 1 point
> 
>  2.Question 2
> 
> Why do we learn a function d(img1,img2)d(img1, img2)d(img1,img2) for face verification? (Select all that apply.) 
> 
> Check
>
    	We need to solve a one-shot learning problem.
	This allows us to learn to recognize a new person given just a single image of that person.
> Correct
> 
> 1 / 1 point
> 
>  3.Question 3
> 
> In order to train the parameters of a face recognition system, it would be reasonable to use a training set comprising 100,000 pictures of 100,000 different persons. 
> 
> Check
 >
 	False
> Correct
> 
> 1 / 1 point
> 
>  4.Question 4
> 
> Which of the following is a correct definition of the triplet loss? Consider that α>0\alpha > 0α>0. (We encourage you to figure out the answer from first principles, rather than just refer to the lecture.) 
> 
> Check
>   
   	max(||f(A)−f(P)||2−||f(A)−f(N)||2+α,0)
> Correct
> 
> 1 / 1 point
> 
>  5.Question 5
> 
> Consider the following Siamese network architecture:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xryVS70VEee3NhLzohKsog_98c778df87f041af9903bd66d2d98bbd_Screen-Shot-2017-10-29-at-6.57.51-PM.png?expiry=1589155200000&hmac=fTvge6J4wXOhRdI7bh9q9KhDm-XQDEgoLKpuBPlFMHE)
> 
> The upper and lower neural networks have different input images, but have exactly the same parameters. 
> 
> Check
>
    True
> Correct
> 
> 1 / 1 point
> 
>  6.Question 6
> 
> You train a ConvNet on a dataset with 100 different classes. You wonder if you can find a hidden unit which responds strongly to pictures of cats. (I.e., a neuron so that, of all the input/training images that strongly activate that neuron, the majority are cat pictures.) You are more likely to find this unit in layer 4 of the network than in layer 1. 
> 
> 
>
    True
> Correct
> 
> 1 / 1 point
> 
>  7.Question 7
> 
> Neural style transfer is trained as a supervised learning task in which the goal is to input two images (xxx), and train a network to output a new, synthesized image (yyy). 
> 
> Check
>
    False
> Correct
> 
> 1 / 1 point
> 
>  8.Question 8
> 
> In the deeper layers of a ConvNet, each channel corresponds to a different feature detector. The style matrix G[l]G^{[l]}G[l] measures the degree to which the activations of different feature detectors in layer lll vary (or correlate) together with each other. 
> 
> Check
>
    True
> Correct
> 
> 1 / 1 point
> 
>  9.Question 9
> 
> In neural style transfer, what is updated in each iteration of the optimization algorithm? 
> 
> Check
>
     The pixel value of G
> Correct
> 
> 1 / 1 point
> 
>  10.Question 10
> 
> You are working with 3D data. You are building a network layer whose input volume has size 32x32x32x16 (this volume has 16 channels), and applies convolutions with 32 filters of dimension 3x3x3 (no padding, stride 1). What is the resulting output volume? 
> 
> Check
>
     30x30x30x32
> Correct
> 
> 1 / 1 point
>
> -- https://www.coursera.org/learn/convolutional-neural-networks/exam/HxEwv/special-applications-face-recognition-neural-style-transfer/attempt?redirectToCover=true#Tunnel Vision Close
