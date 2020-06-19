# Natural Language Processing & Word Embeddings
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> Suppose you learn a word embedding for a vocabulary of 10000 words. Then the embedding vectors should be 10000 dimensional, so as to capture the full range of variation and meaning in those words. 
> 
>  True 
> 

      False 
> 
> Check
> 
> Correct
> 
> The dimension of word vectors is usually smaller than the size of the vocabulary. Most common sizes for word vectors ranges between 50 and 400.
> 
> 1 / 1 point
> 
>  2.Question 2
> 
> What is t-SNE? 
> 
>  A linear transformation that allows us to solve analogies on word vectors 
>

      A non-linear dimensionality reduction technique 
> 
>  A supervised learning algorithm for learning word embeddings 
> 
>  An open-source sequence modeling library 
> 
> Check
> 
> Correct
> 
> Yes
> 
> 1 / 1 point
> 
>  3.Question 3
> 
> Suppose you download a pre-trained word embedding which has been trained on a huge corpus of text. You then use this word embedding to train an RNN for a language task of recognizing if someone is happy from a short snippet of text, using a small training set.
> 
> x (input text)y (happy?)I'm feeling wonderful today!1I'm bummed my cat is ill.0Really enjoying this!1
> 
> Then even if the word “ecstatic” does not appear in your small training set, your RNN might reasonably be expected to recognize “I’m ecstatic” as deserving a label y=1y = 1y=1. 
> 

      True 
> 
>  False 
> 
> Check
> 
> Correct
> 
> Yes, word vectors empower your model with an incredible ability to generalize. The vector for "ecstatic would contain a positive/happy connotation which will probably make your model classified the sentence as a "1".
> 
> 1 / 1 point
> 
>  4.Question 4
> 
> Which of these equations do you think should hold for a good word embedding? (Check all that apply) 
> 

      eboy−egirl≈ebrother−esister
> 
> Check
> 
> Correct
> 
> Yes!
> 
>  eboy−egirl≈esister−ebrother
>

      eboy−ebrother≈egirl−esister 
> 
> Check
> 
> Correct
> 
> Yes!
> 
>  eboy−ebrother≈esister−egirle_{boy} - e_{brother} \approx e_{sister} - e_{girl}eboy​−ebrother​≈esister​−egirl​ 
> 
> 1 / 1 point
> 
>  5.Question 5
> 
> Let EEE be an embedding matrix, and let o1234o_{1234}o1234​ be a one-hot vector corresponding to word 1234\. Then to get the embedding of word 1234, why don’t we call E∗o1234E * o_{1234}E∗o1234​ in Python? 
> 

      It is computationally wasteful. 
> 
>  The correct formula is ET∗o1234E^T* o_{1234}ET∗o1234​. 
> 
>  This doesn’t handle unknown words (<UNK>). 
> 
>  None of the above: calling the Python snippet as described above is fine. 
> 
> Check
> 
> Correct
> 
> Yes, the element-wise multiplication will be extremely inefficient.
> 
> 1 / 1 point
> 
>  6.Question 6
> 
> When learning word embeddings, we create an artificial task of estimating P(target∣context)P(target \mid context)P(target∣context). It is okay if we do poorly on this artificial prediction task; the more important by-product of this task is that we learn a useful set of word embeddings. 
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
>  7.Question 7
> 
> In the word2vec algorithm, you estimate P(t∣c)P(t \mid c)P(t∣c), where ttt is the target word and ccc is a context word. How are ttt and ccc chosen from the training set? Pick the best answer. 
> 
>  ccc is the one word that comes immediately before ttt. 
> 
>  ccc is the sequence of all the words in the sentence before ttt. 
> 
>  ccc is a sequence of several words immediately before ttt. 
> 

      ccc and ttt are chosen to be nearby words. 
> 
> Check
> 
> Correct
> 
> 1 / 1 point
> 
>  8.Question 8
> 
> Suppose you have a 10000 word vocabulary, and are learning 500-dimensional word embeddings. The word2vec model uses the following softmax function:
> 
> P(t∣c)=eθtTec∑t’=110000eθt’TecP(t \mid c) = \frac{e^{\theta_t^T e_c}}{\sum_{t’=1}^{10000} e^{\theta_{t’}^Te_c}}P(t∣c)=∑t’=110000​eθt’T​ec​eθtT​ec​​
> 
> Which of these statements are correct? Check all that apply. 
> 

      θt\theta_tθt​ and ece_cec​ are both 500 dimensional vectors. 
> 
> Check
> 
> Correct
> 
>  θt\theta_tθt​ and ece_cec​ are both 10000 dimensional vectors. 
> 

      θt\theta_tθt​ and ece_cec​ are both trained with an optimization algorithm such as Adam or gradient descent. 
> 
> Check
> 
> Correct
> 
>  After training, we should expect θt\theta_tθt​ to be very close to ece_cec​ when ttt and ccc are the same word. 
> 
> 1 / 1 point
> 
>  9.Question 9
> 
> Suppose you have a 10000 word vocabulary, and are learning 500-dimensional word embeddings.The GloVe model minimizes this objective:
> 
> min⁡∑i=110,000∑j=110,000f(Xij)(θiTej+bi+bj’−logXij)2\min \sum_{i=1}^{10,000} \sum_{j=1}^{10,000} f(X_{ij}) (\theta_i^T e_j + b_i + b_j’ - log X_{ij})^2min∑i=110,000​∑j=110,000​f(Xij​)(θiT​ej​+bi​+bj​’−logXij​)2
> 
> Which of these statements are correct? Check all that apply. 
> 
>  θi\theta_iθi​ and eje_jej​ should be initialized to 0 at the beginning of training. 
> 

      θi\theta_iθi​ and eje_jej​ should be initialized randomly at the beginning of training. 
> 
> Check
> 
> Correct
> 
    
      XijX_{ij}Xij​ is the number of times word j appears in the context of word i. 
> 
> Check
> 
> Correct
> 

      The weighting function f(.)f(.)f(.) must satisfy f(0)=0f(0) = 0f(0)=0. 
> 
> Check
> 
> Correct
> 
> The weighting function helps prevent learning only from extremely common word pairs. It is not necessary that it satisfies this function.
> 
> 1 / 1 point
> 
>  10.Question 10
> 
> You have trained word embeddings using a text dataset of m1m_1m1​ words. You are considering using these word embeddings for a language task, for which you have a separate labeled dataset of m2m_2m2​ words. Keeping in mind that using word embeddings is a form of transfer learning, under which of these circumstance would you expect the word embeddings to be helpful? 
> 

      m1 >> m2 
> 
>  m1 << m2 
> 
> Check
> 
> Correct
>
> -- https://www.coursera.org/learn/nlp-sequence-models/exam/nIlU0/natural-language-processing-word-embeddings/attempt?redirectToCover=true#Tunnel Vision Close
