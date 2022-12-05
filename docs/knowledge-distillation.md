Knowledge Distillation is a technique of compressing a model which allows it to fit a computer that may 
not have accelerator (GPUs) or enough memory to fit the original baseline model.

According to experts, a very simple way to improve the performance of almost any machine learning algorithm
is to train many different models on the same data and then to average their predictions. Unfortunately, 
making predictions using a whole ensemble of models is cumbersome and may be too computationally expensive 
to allow deployment to a large number of users, especially if the individual models are large neural nets.

The experts also have shown that it is possible to compress the knowledge in an ensemble into a single 
model which is much easier to deploy and we develop this approach further using a different compression 
technique. We achieve some surprising results on MNIST and we show that we can significantly improve the 
acoustic model of a heavily used commercial system by distilling the knowledge in an ensemble of models into 
a single model. We also introduce a new type of ensemble composed of one or more full models and many 
specialist models which learn to distinguish fine-grained classes that the full models confuse. Unlike a 
mixture of experts, these specialist models can be trained rapidly and in parallel.

In Knowledge Distillation, the compressed model is trained to mimic a pre-trained, larger model. This 
training setting is also referred to as “teacher-student”, where the large model is the teacher and the 
small model is the student.

Knowledge Distillation is often used to fine-tune the pruned model.

![image](https://user-images.githubusercontent.com/94308793/205538928-f6ee5765-ee6e-4942-8ad5-b7477d4507b5.png)

The results obtained from Knowledge Distillation should be a much more efficient run time exection of the 
model with a minimized amount of loss.

For my model, I was unable to obtain results because even with model compression, I found that Google Colab 
would crash each time I would attempt to run my code. I expect that it would be similar to my previous 
results obtained through other milestones and would look something like the following:

![image](https://user-images.githubusercontent.com/94308793/205539555-86f30f67-785a-4d1c-b122-745197fd427b.png)
