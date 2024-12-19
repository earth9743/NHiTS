# NHiTS

실험 장비 : MacBook Pro 13-inch, M1, 2020
사양 : Apple M1
OS : Sonoma 14.6.1

가상환경
- conda
- Python ver : 3.9.21

필요 라이브러리 및 버전
  1. coreforecast>=0.0.6 
  2. fsspec numpy>=1.21.6 
  3. pandas>=1.3.5 torch>=2.0.0 
  4. pytorch-lightning>=2.0.0 
  5. ray[tune]>=2.2.0 
  6.optuna utilsforecast>=0.2.3

필요 dataset
  1. neuralforecast
  2. datasetsforecast

실행방법
  kan_benchmark
  1. experiments/kan_benchmark/run_experiment.py 이동
  2. 터미널에 python run_experiment.py --dataset 'M3-monthly' 입력
     -- --dataset 뒤에 'M3-monthly' or M3-quarterly .... 입력 가능
     -- --dataset : ['M3-yearly', 'M3-quarterly', 'M3-monthly', 'M4-yearly', 'M4-quarterly', 'M4-monthly', 'M4-weekly', 'M4-daily', 'M4-  hourly']
     
  long_horizon
  1. experiments/long_horizon/run_experiment.py 이동
  2. 터미널에 python run_nhits.py --dataset 'ETTh1' --horizon 96 --num_samples 20
     -- --dataset ['ETTh1', 'ETTh2', 'ETTm1', 'ETTm2']
     -- --horizon [96, 192, 336, 720]
     -- --num_samples 20 권장 (https://nixtlaverse.nixtla.io/neuralforecast/docs/tutorials/getting_started_complete.html) 참조
