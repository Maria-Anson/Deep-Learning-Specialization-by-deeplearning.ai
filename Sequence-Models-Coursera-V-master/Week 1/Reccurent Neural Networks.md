> ## Recurrent Neural Networks
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> Suppose your training examples are sentences (sequences of words). Which of the following refers to the jthj^{th}jth word in the ithi^{th}ith training example? 
> 

      x(i)<j> 
> 
>  **x<i>(j)** 
> 
>  **x(j)<i>** 
> 
>  **x<j>(i)** 
> 
> Check
> 
> Correct
> 
> We index into the ithi^{th}ith row first to get the ithi^{th}ith training example (represented by parentheses), then the jthj^{th}jth column to get the jthj^{th}jth word (represented by the brackets).
> 
> 1 / 1 point
> 
>  2.Question 2
> 
> Consider this RNN:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/WVhjoPCuEee5Rg5IFJ7l8g_a7b6030c6e5a53b431fee7aaabecd9bd_Screen-Shot-2018-01-03-at-5.48.26-PM.png?expiry=1589500800000&hmac=ngblJiaDqWhL_TLThYYPgjeujYhbrCmLlh6Cz0S2ZcU)
> 
> This specific type of architecture is appropriate when: 
> 

      Tx=Ty
> 
>  **Tx<Ty** 
> 
>  **Tx>Ty* 
> 
>  **Tx=1** 
> 
> Check
> 
> Correct
> 
> It is appropriate when every input should be matched to an output.
> 
> 1 / 1 point
> 
>  3.Question 3
> 
> To which of these tasks would you apply a many-to-one RNN architecture? (Check all that apply).
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/K59CdPCvEee7LQrRPHr2wA_4549ad1b1b590371eb3502e158a02447_Screen-Shot-2018-01-03-at-5.54.27-PM.png?expiry=1589500800000&hmac=BqGM4IsBxPd_dgWmVHSawBnWUZbwoii1XbRdw1IDaiw) 
> 
>  Speech recognition (input an audio clip and output a transcript) 
> 
    
    >  Sentiment classification (input a piece of text and output a 0/1 to denote positive or negative sentiment) 
> 
> Check
> 
> Correct
> 
> Correct!
> 
>  Image classification (input an image and output a label) 
> 

    >  Gender recognition from speech (input an audio clip and output a label indicating the speaker’s gender) 
> 
> Check
> 
> Correct
> 
> Correct!
> 
> 1 / 1 point
> 
>  4.Question 4
> 
> You are training this RNN language model.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cxeeLPCvEee7YRLKCWJ4hg_bca1b05c70eece156b470abb2d0f0cad_Screen-Shot-2018-01-03-at-5.56.30-PM.png?expiry=1589500800000&hmac=60XyUk6a_SsIhWgqOPrhejklvsqvzj2eLzidqtZ4Wio)
> 
> At the ttht^{th}tth time step, what is the RNN doing? Choose the best answer. 
> 
>  Estimating P(y<1>,y<2>,…,y<t−1>)P(y^{<1>}, y^{<2>}, …, y^{<t-1>})P(y<1>,y<2>,…,y<t−1>) 
> 
>  Estimating P(y<t>)P(y^{<t>})P(y<t>) 
> 

    >  Estimating P(y<t>∣y<1>,y<2>,…,y<t−1>)P(y^{<t>} \mid y^{<1>}, y^{<2>}, …, y^{<t-1>})P(y<t>∣y<1>,y<2>,…,y<t−1>) 
> 
>  Estimating P(y<t>∣y<1>,y<2>,…,y<t>)P(y^{<t>} \mid y^{<1>}, y^{<2>}, …, y^{<t>})P(y<t>∣y<1>,y<2>,…,y<t>) 
> 
> Check
> 
> Correct
> 
> Yes, in a language model we try to predict the next step based on the knowledge of all prior steps.
> 
> 1 / 1 point
> 
>  5.Question 5
> 
> You have finished training a language model RNN and are using it to sample random sentences, as follows:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zOkWE_CvEee5Rg5IFJ7l8g_f36533d67eb6590d5bcb7021d88493eb_Screen-Shot-2018-01-03-at-5.58.53-PM.png?expiry=1589500800000&hmac=c3BXDVi1eg0eo5Z19g2lHAeimZXJaPyGGja6IUZSjGE)
> 
> What are you doing at each time step ttt? 
> 
>  (i) Use the probabilities output by the RNN to pick the highest probability word for that time-step as y^<t>\hat{y}^{<t>}y^​<t>. (ii) Then pass the ground-truth word from the training set to the next time-step. 
> 
>  (i) Use the probabilities output by the RNN to randomly sample a chosen word for that time-step as y^<t>\hat{y}^{<t>}y^​<t>. (ii) Then pass the ground-truth word from the training set to the next time-step. 
> 
>  (i) Use the probabilities output by the RNN to pick the highest probability word for that time-step as y^<t>\hat{y}^{<t>}y^​<t>. (ii) Then pass this selected word to the next time-step. 
> 
    
    >  (i) Use the probabilities output by the RNN to randomly sample a chosen word for that time-step as y^<t>\hat{y}^{<t>}y^​<t>. (ii) Then pass this selected word to the next time-step. 
> 
> Check
> 
> Correct
> 
> Yes!
> 
> 1 / 1 point
> 
>  6.Question 6
> 
> You are training an RNN, and find that your weights and activations are all taking on the value of NaN (“Not a Number”). Which of these is the most likely cause of this problem? 
> 
>  Vanishing gradient problem. 
> 

    >  Exploding gradient problem. 
> 
>  ReLU activation function g(.) used to compute g(z), where z is too large. 
> 
>  Sigmoid activation function g(.) used to compute g(z), where z is too large. 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  7.Question 7
> 
> Suppose you are training a LSTM. You have a 10000 word vocabulary, and are using an LSTM with 100-dimensional activations a<t>a^{<t>}a<t>. What is the dimension of Γu\Gamma_uΓu​ at each time step? 
> 
>  1 
> 

    >  100 
> 
>  300 
> 
>  10000 
> 
> Check
> 
> Correct
> 
> Correct, Γu\Gamma_uΓu​ is a vector of dimension equal to the number of hidden units in the LSTM.
> 
> 1 / 1 point
> 
>  8.Question 8
> 
> Here’re the update equations for the GRU.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/y-VsavCwEeeVOQpGYM3DAA_b10afdb5d35702d711338d5b72ce5be7_Screen-Shot-2018-01-03-at-6.05.56-PM.png?expiry=1589500800000&hmac=NtMgQ-QD6aaUrWY_iJJ0scDyuOW-sZo8IK2EGIGQVp4)
> 
> Alice proposes to simplify the GRU by always removing the Γu\Gamma_uΓu​. I.e., setting Γu\Gamma_uΓu​ = 1\. Betty proposes to simplify the GRU by removing the Γr\Gamma_rΓr​. I. e., setting Γr\Gamma_rΓr​ = 1 always. Which of these models is more likely to work without vanishing gradient problems even when trained on very long input sequences? 
> 
>  Alice’s model (removing Γu\Gamma_uΓu​), because if Γr≈0\Gamma_r \approx 0Γr​≈0 for a timestep, the gradient can propagate back through that timestep without much decay. 
> 
>  Alice’s model (removing Γu\Gamma_uΓu​), because if Γr≈1 \Gamma_r \approx 1Γr​≈1 for a timestep, the gradient can propagate back through that timestep without much decay. 
> 
    
    >  Betty’s model (removing Γr\Gamma_rΓr​), because if Γu≈0\Gamma_u \approx 0Γu​≈0 for a timestep, the gradient can propagate back through that timestep without much decay. 
> 
>  Betty’s model (removing Γr\Gamma_rΓr​), because if Γu≈1\Gamma_u \approx 1Γu​≈1 for a timestep, the gradient can propagate back through that timestep without much decay. 
> 
> Check
> 
> Correct
> 
> Yes. For the signal to backpropagate without vanishing, we need c<t>c^{<t>}c<t> to be highly dependant on c<t−1>c^{<t-1>}c<t−1>.
> 
> 1 / 1 point
> 
>  9.Question 9
> 
> Here are the equations for the GRU and the LSTM:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ZJgnEfCxEeeVOQpGYM3DAA_2552c64114ba9a4a065a54e8e4855b39_Screen-Shot-2018-01-03-at-6.10.24-PM.png?expiry=1589500800000&hmac=JHXR072HgheWFF55haS-CgmpdCO_WcYRcRFMGe6y6Lw)
> 
> From these, we can see that the Update Gate and Forget Gate in the LSTM play a role similar to _______ and ______ in the GRU. What should go in the the blanks? 
> 

    >  Γu\Gamma_uΓu​ and 1−Γu1-\Gamma_u1−Γu​ 
> 
>  Γu\Gamma_uΓu​ and Γr\Gamma_rΓr​ 
> 
>  1−Γu1-\Gamma_u1−Γu​ and Γu\Gamma_uΓu​ 
> 
>  Γr\Gamma_rΓr​ and Γu\Gamma_uΓu​ 
> 
> Check
> 
> Correct
> 
> Yes, correct!
> 
> 1 / 1 point
> 
>  10.Question 10
> 
> You have a pet dog whose mood is heavily dependent on the current and past few days’ weather. You’ve collected data for the past 365 days on the weather, which you represent as a sequence as x<1>,…,x<365>x^{<1>}, …, x^{<365>}x<1>,…,x<365>. You’ve also collected data on your dog’s mood, which you represent as y<1>,…,y<365>y^{<1>}, …, y^{<365>}y<1>,…,y<365>. You’d like to build a model to map from x→yx \rightarrow yx→y. Should you use a Unidirectional RNN or Bidirectional RNN for this problem? 
> 
>  Bidirectional RNN, because this allows the prediction of mood on day t to take into account more information. 
> 
>  Bidirectional RNN, because this allows backpropagation to compute more accurate gradients. 
> 

    >  Unidirectional RNN, because the value of y<t>y^{<t>}y<t> depends only on x<1>,…,x<t>x^{<1>}, …, x^{<t>}x<1>,…,x<t>, but not on x<t+1>,…,x<365>x^{<t+1>}, …, x^{<365>}x<t+1>,…,x<365> 
> 
>  Unidirectional RNN, because the value of y<t>y^{<t>}y<t> depends only on x<t>x^{<t>}x<t>, and not other days’ weather. 
> 
> Check
> 
> Correct
> 
> Yes!
>
> -- https://www.coursera.org/learn/nlp-sequence-models/exam/e4bJR/recurrent-neural-networks/attempt?redirectToCover=true#Tunnel Vision Close
