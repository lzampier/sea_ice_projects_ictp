# sea_ice_projects_ictp

Repository containing useful information and scripts for the projects of the summer school on Polar Climates.

## Log onto ictp Linux cluster, replace user with your login name

ssh user@argo-login1.ictp.it

or 

ssh user@argo-login2.ictp.it

## Run once to get stated

### Run the script to modify your .bashrc file to access software for this course

/home/esp-shared-a/Distribution/Workshops/PolarClimate_2024/argo_run_me_first

source ~/.bashrc

### Install miniconda

wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

chmod 744 ./Miniconda3-latest-Linux-x86_64.sh

./Miniconda3-latest-Linux-x86_64.sh

source ./.bashrc

### Clone code from Github specific to our project, and install 
the postprocessing conda environment with all the required packages

git clone https://github.com/lzampier/sea_ice_projects_ictp.git

conda env create -f sea_ice_projects_ictp/envs/project_env.yaml

## Start Jupyter, substitute your favorite 4 digit number for the port

jupyter notebook --no-browser --port=9994

### now on youor laptop, substitue your port number and user name. Be sure login1 or login2 matches the one you used to get on to  ictpwhere you ran jupyter

ssh -N -f -L localhost:9994:localhost:9994 user@argo-login1.ictp.it
 