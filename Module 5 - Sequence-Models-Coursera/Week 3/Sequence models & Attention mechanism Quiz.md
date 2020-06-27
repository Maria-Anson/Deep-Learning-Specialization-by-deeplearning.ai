# Sequence models & Attention mechanism
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> Consider using this encoder-decoder model for machine translation.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qXy2GwVdEeirxApwydYI3g_563d74fd24e481f841070e81da7ee0aa_Screen-Shot-2018-01-29-at-5.33.03-PM.png?expiry=1590278400000&hmac=rdLht8e3Iyn1UKcOt34JsCYzHl6hW8-VbLCkBtgEdUk)
> 
> This model is a “conditional language model” in the sense that the encoder portion (shown in green) is modeling the probability of the input sentence xxx. 
> 
>  True 
> 

      False 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  2.Question 2
> 
> In beam search, if you increase the beam width BBB, which of the following would you expect to be true? Check all that apply. 
> 

      Beam search will run more slowly. 
> 
> Check
> 
> Correct
> 

      Beam search will use up more memory. 
> 
> Check
> 
> Correct
> 

      Beam search will generally find better solutions (i.e. do a better job maximizing P(y∣x)P(y \mid x)P(y∣x)) 
> 
> Check
> 
> Correct
> 
>  Beam search will converge after fewer steps. 
> 
> 1 / 1 point
> 
>  3.Question 3
> 
> In machine translation, if we carry out beam search without using sentence normalization, the algorithm will tend to output overly short translations. 
> 

      True 
> 
>  False 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  4.Question 4
> 
> Suppose you are building a speech recognition system, which uses an RNN model to map from audio clip xxx to a text transcript yyy. Your algorithm uses beam search to try to find the value of yyy that maximizes P(y∣x)P(y \mid x)P(y∣x).
> 
> On a dev set example, given an input audio clip, your algorithm outputs the transcript y^=\hat{y}=y^​= “I’m building an A Eye system in Silly con Valley.”, whereas a human gives a much superior transcript y∗=y^* =y∗= “I’m building an AI system in Silicon Valley.”
> 
> According to your model,
> 
> P(y^∣x)=1.09∗10−7P(\hat{y} \mid x) = 1.09*10^-7P(y^​∣x)=1.09∗10−7
> 
> P(y∗∣x)=7.21∗10−8P(y^* \mid x) = 7.21*10^-8P(y∗∣x)=7.21∗10−8
> 
> Would you expect increasing the beam width B to help correct this example? 
> 

      No, because P(y∗∣x)≤P(y^∣x)P(y^* \mid x) \leq P(\hat{y} \mid x)P(y∗∣x)≤P(y^​∣x) indicates the error should be attributed to the RNN rather than to the search algorithm. 
> 
>  No, because P(y∗∣x)≤P(y^∣x)P(y^* \mid x) \leq P(\hat{y} \mid x)P(y∗∣x)≤P(y^​∣x) indicates the error should be attributed to the search algorithm rather than to the RNN. 
> 
>  Yes, because P(y∗∣x)≤P(y^∣x)P(y^* \mid x) \leq P(\hat{y} \mid x)P(y∗∣x)≤P(y^​∣x) indicates the error should be attributed to the RNN rather than to the search algorithm. 
> 
>  Yes, because P(y∗∣x)≤P(y^∣x)P(y^* \mid x) \leq P(\hat{y} \mid x)P(y∗∣x)≤P(y^​∣x) indicates the error should be attributed to the search algorithm rather than to the RNN. 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  5.Question 5
> 
> Continuing the example from Q4, suppose you work on your algorithm for a few more weeks, and now find that for the vast majority of examples on which your algorithm makes a mistake, P(y∗∣x)>P(y^∣x) P(y^* \mid x) > P(\hat{y} \mid x)P(y∗∣x)>P(y^​∣x). This suggest you should focus your attention on improving the search algorithm. 
> 
    
      True. 
> 
>  False. 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  6.Question 6
> 
> Consider the attention model for machine translation.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ZdQLWgVeEei_ZQ6W1G11dA_5ea60f98993ef910d93aaf10c16c4cc9_Screen-Shot-2018-01-29-at-5.38.58-PM.png?expiry=1590278400000&hmac=QLQckpMi-pADdBemLNOJ5HMv7hnsHGPQ4POQSqYGzOo)
> 
> Further, here is the formula for α<t,t’>\alpha^{<t,t’>}α<t,t’>.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/kBdw_AVeEeiIOArs7r1YtA_da38112b640e4901fbbf692a9e6611be_Screen-Shot-2018-01-29-at-5.39.03-PM.png?expiry=1590278400000&hmac=-GZ9cJdU-J0xzOKZ3cafzmXyBN0Uo3G5TPHKCtbOt3w)
> 
> Which of the following statements about α<t,t’>\alpha^{<t,t’>}α<t,t’> are true? Check all that apply. 
> 
  
      We expect α<t,t’>\alpha^{<t,t’>}α<t,t’> to be generally larger for values of a<t’>a^{<t’>}a<t’> that are highly relevant to the value the network should output for y<t>y^{<t>}y<t>. (Note the indices in the superscripts.) 
> 
> Check
> 
> Correct
> 
>  We expect α<t,t’>\alpha^{<t,t’>}α<t,t’> to be generally larger for values of a<t>a^{<t>}a<t> that are highly relevant to the value the network should output for y<t’>y^{<t’>}y<t’>. (Note the indices in the superscripts.) 
> 
>  ∑tα<t,t’>=1\sum_{t} \alpha^{<t,t’>} = 1∑t​α<t,t’>=1 (Note the summation is over ttt.) 
> 
    
      ∑t’α<t,t’>=1\sum_{t’} \alpha^{<t,t’>} = 1∑t’​α<t,t’>=1 (Note the summation is over t’t’t’.) 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  7.Question 7
> 
> The network learns where to “pay attention” by learning the values e<t,t’>e^{<t,t’>}e<t,t’>, which are computed using a small neural network:
> 
> We can't replace s<t−1>s^{<t-1>}s<t−1> with s<t> s^{<t>}s<t> as an input to this neural network. This is because s<t>s^{<t>}s<t> depends on α<t,t’>\alpha^{<t,t’>}α<t,t’> which in turn depends on e<t,t’>e^{<t,t’>}e<t,t’>; so at the time we need to evalute this network, we haven’t computed s<t>s^{<t>}s<t> yet. 
> 
    
    True 
> 
>  False 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  8.Question 8
> 
> Compared to the encoder-decoder model shown in Question 1 of this quiz (which does not use an attention mechanism), we expect the attention model to have the greatest advantage when: 
> 
    
      The input sequence length TxT_xTx​ is large. 
> 
>  The input sequence length TxT_xTx​ is small. 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  9.Question 9
> 
> Under the CTC model, identical repeated characters not separated by the “blank” character (_) are collapsed. Under the CTC model, what does the following string collapse to?
> 
> __c_oo_o_kk___b_ooooo__oo__kkk 
> 
>  cokbok 
> 

      cookbook 
> 
>  cook book 
> 
>  coookkboooooookkk 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  10.Question 10
> 
> In trigger word detection, x<t>x^{<t>}x<t> is: 
> 
    
    Features of the audio (such as spectrogram features) at time ttt. 
> 
>  The ttt-th input word, represented as either a one-hot vector or a word embedding. 
> 
>  Whether the trigger word is being said at time ttt. 
> 
>  Whether someone has just finished saying the trigger word at time ttt. 
> 
> Check
> 
> Correct
>
> -- https://www.coursera.org/learn/nlp-sequence-models/exam/4CCc4/sequence-models-attention-mechanism/attempt?redirectToCover=true#Tunnel Vision Close
