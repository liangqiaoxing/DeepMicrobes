# DeepMicrobes
DeepMicrobes: a deep learning architecture for taxonomic classification of shotgun metagenomic reads

## Installation

#### Dependencies
DeepMicrobes relies on the following Python modules:
* biopython
* numpy
* tensorflow
* absl

#### Clone
To start working with the code:

    git clone https://github.com/liangqiaoxing/DeepMicrobes.git
    
## Usage

#### Training

    python DeepMicrobes.py --train_epochs=${EPOCH} --batch_size=${BATCH_SIZE} \
                           --lr=${LEARNING_RATE} --lr_decay=${LEARNING_RATE_DECAY} \
                           --num_classes=${NUM_CLASSES} --keep_prob=${KEEP_PROB} \
                           --input_tfrec=${TFRECORD} --model_dir=${MODEL_DIR} \
                           --running_mode=train
                           
#### Evaluation

    python DeepMicrobes.py --batch_size=${BATCH_SIZE} --num_classes=${NUM_CLASSES} \
                           --input_tfrec=${TFRECORD} --model_dir=${MODEL_DIR} \
                           --running_mode=eval
                           

#### Prediction

For paired-end data:
    
    python DeepMicrobes.py --batch_size=${BATCH_SIZE} --num_classes=${NUM_CLASSES} \
                           --input_tfrec=${TFRECORD} --model_dir=${MODEL_DIR} \
                           --label_file=/path/to/label2taxid.txt --translate=True \
                           --pred_out=/path/to/pred_out_prefix \
                           --running_mode predict_paired_class

For single-end data:

    python DeepMicrobes.py --batch_size=${BATCH_SIZE} --num_classes=${NUM_CLASSES} \
                           --input_tfrec=${TFRECORD} --model_dir=${MODEL_DIR} \
                           --label_file=/path/to/label2taxid.txt --translate=True \
                           --pred_out=/path/to/pred_out_prefix \
                           --running_mode predict_single_class
                           
#### Report
                           
