## Converting sequences to TFRecord

### One-hot encoding

    seq2tfrec_onehot.py --input_seq=input.fasta \
                        --output_tfrec=output.tfrec \
                        --label=/path/to/label2taxid.txt \
                        --is_train=True \
                        --seq_type=fasta
  

### K-mer embedding

    export PYTHONPATH=$PYTHONPATH:/path/to/DeepMicrobes
  
    seq2tfrec_kmer.py --input_seq=input.fasta \
                      --output_tfrec=output.tfrec \
                      --label=/path/to/label2taxid.txt \
                      --is_train=True \
                      --seq_type=fasta \
                      --kmer=12 \
                      --vocab=/path/to/token_12mer


The vocabulary file of merged 12-mers can be downloaded [here](https://drive.google.com/open?id=1QPV9Mdsrk8rHRvinKoMY4s-UCKyKK3xZ). 
