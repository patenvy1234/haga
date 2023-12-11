pre-steps

cd Desktop/haga/src -> basically sab src folder me hai toh usme jake run karna sab 


# download karo idhar se data 
https://drive.google.com/open?id=1BWBN1coTWGBqrWoOfRc5dhojPHhatbYs

after then unzip it aur bert_data vale folder me sara data daal do 

python3 train.py -task ext -mode train -bert_data_path ../bert_data -ext_dropout 0.1 -model_path MODEL_PATH -lr 2e-3 -visible_gpus -1 -report_every 50 -save_checkpoint_steps 1000 -batch_size 3000 -train_steps 50000 -accum_count 2 -log_file ../logs/ext_bert_cnndm -use_interval true -warmup_steps 10000 -max_pos 512


aaab yeh pura command run karo to download BERT model bas after downloading ek "temp" naam ka folder generate ho jayega jaha BERT ka model cached rahega


python3 train.py -task ext -mode train -bert_data_path ../bert_data -ext_dropout 0.1 -model_path MODEL_PATH -lr 2e-3 -visible_gpus -1 -report_every 50 -save_checkpoint_steps 1000 -batch_size 3000 -train_steps 50000 -accum_count 2 -log_file ../logs/ext_bert_cnndm -use_interval true -warmup_steps 10000 -max_pos 512


abb yeh run karo for training isme cached BERT MODEL use hoga direct 
