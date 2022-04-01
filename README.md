# CS5260_Colossalai_LR_Range_Test

Colossalai is a distributed training framework developed by Prof Yang You’s team. We will take use of it in this assignment, but code frame is given so you don’t have to dive deep. It can enable different kind of distributed training easily (including data parallel, tensor parallel, pipeline parallel and so on) and provides efficient memory handling.

Learning rate range test is a method proposed by Leslie N. Smith in paper Super-Convergence: Very Fast Training of Neural Networks Using Large Learning Rates. The idea is: before normally training your model to convergence, first train your model with exponentially increasing learning rate (increase with batch step) for several epochs, and observe the loss curve. Usually the loss will first keep unchanged, and then go down, and finally explode. The learning rate corresponding to loss going down will be usable LR, and explosion part is not usable. Depending on your chosen optimizer and learning rate scheduling, this method can give you reference for LR choice region, and for some of the settings this method can serve as a super fast tuning method with high performance.

In this assignment, a file named Colossalai_lr_range_test.ipynb will be given, and it contains the code frame for LR range test part.
