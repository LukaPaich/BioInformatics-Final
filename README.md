# Free University Bioinformatics Final

### Using finetuning to identify introns/exons/boundaries in chromosomes
### Based on this <a href="https://arxiv.org/pdf/2311.12884">Paper</a>

  In this project we aim to recreate the results of the above mentioned paper in order to accurately predict whether sequences of DNA contain intron/exon boundary regions.
The paper uses a custom deep learning model to achieve very high (~95% F1 score) accuracy on test data, and we aim to achieve that using a different model.

  To be more specific, in the paper they used a custom model built using LSTM and attention to accurately convey the context of the DNA sequences to identify motifs. They also use simple models like CNNs (Convolutional Neural Networks and RNNs (Recurrent Neural Networks) to compare the accuracy of their custom 'DeepDeCode' model. In this project we use a pre-trained model <a href="https://huggingface.co/zhihan1996/DNABERT-2-117M">DNABERT-2</a> to fine-tune it to fit the papers problem and try to match the accuracy and scores of their custom trained model. In addition we also aim to make the fine-tuning require a lot less GPU power and leverage the time spent pre-training an existing model.
  
  In addition, we also rewrote the data gathering and generating pipeline to use modern Python version and be simple to use. The Papers <a href="https://github.com/asmitapoddar/Deep-Learning-DNA-Sequences">Github Repository</a> has a pretty outdated pipeline for gathering and generating datasets for this particular problem. Our reworked version has easier customizability, less required dependencies, and is much easier to use. We suspect that this pipeline can be used for other tasks as well.

