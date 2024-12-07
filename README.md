# CONDA CHEATS ----------------------------------------------------------------------
* To clone an environment: conda create --name new_env_name --clone env_name_to_clone
* conda env list
* conda env remove --name <env>
* conda env create -f something.yaml
* conda create --name <env>
* conda env update --file something.yaml --prune
* conda install -c conda-forge numpy==1.19.5
* conda env export > environment.yml

* pip install -r requirements.txt
* conda list -e > requirements.txt

# UBUNTU CHEATS --------------------------------------------------------------------
* Create txt File: cat > something.txt (Then click 'enter' write something and then ctrl+D)
## Convert jpeg to png
* find . -name "*.jpeg" -exec mogrify -format png {} \\;
## Check the extensions for png
* find . -type f -name "*.png"
## Delete jpeg files
* find . -type f -iname \*.jpeg -delete
## Copy files
* cp a_folder/b_folder/*png c_folder/d_folder/ (To move them use 'mv' instead of 'cp')
## Count files & Count json files
* ls | wc -l
* ls *.json | wc -l
## Cut a video
* ffmpeg -ss 00:00:00(Where to start) -t 00:01:00(duration) -i video.mp4 -vcodec copy copy_video.mp4
## Concat A Video
*  for f in *.mp4; do echo "file '$f'" >> videos.txt; done
*  ffmpeg -f concat -i videos.txt -c copy output.mp4
## Remove blank spaces
* rename "s/ *//g" *
## Replace spaces in file names with underscore
* rename 's/\s+/_/g' *
## Adding 'office_' to the name of the files
* rename 's/^/office_/' *
## Rename 'chessboard-R' with 'right' in names of files
* rename "s/chessboard-R/right/g" *
## Learn your IP adress
* hostname -I
## Read a file via command line and edit it
* nano abc.txt
* cat abc.txt (only reading via terminal)
## Secure copy from machine A (1.1.1.1) to machine B(2.2.2.2)
* scp frodo@1.1.1.1:/home sam@2.2.2.2:/home
## Delete a file
* rm scenario.zip
## Zip and unzip a folder
* zip -r frodo.zip frodo
* unzip frodo.zip -d frodo
## Video stream from the webcam
* ffplay /dev/video0
## Information about a video
* ffmpeg -i filename
## Open bash profile
* nano ~/.bash_profile
## To Check the ROS2 Version
* printenv ROS_DISTRO
## Zip a folder with Password
* zip -r -e the_zip_name.zip the_folder/

# GIT CHEATS ----------------------------------------------------------------------------
* git branch
* git add something.py
* git commit -m "something something"
* git push 
## To stash the changes
* git add something.py
* git stash 
* git pull
* git stash pop
## Preventing certificate verification error
* git -c http.sslVerify=false clone https://github.com/opencv/opencv.git
  
  
# OTHER CHEATS ----------------------------------------------------------------------
* Check the camera: v4l2-ctl --list-devices
* Disable Camera: sudo modprobe -r uvcvideo
* Enable Camera: sudo modporbe uvcvideo

# PYTHON CHEATS --------------------------------------------------------------------
## Append a txt file in the project
* txt_file = open('path_to_txt_file.txt', 'a')
  
  txt_file.write(f'\nThe counter: {detection.data}')
  
  txt_file.close()

##  Create EXE 
  pyinstaller --onefile --console `
  --onefile --console `
 --hidden-import=tkinter `
 --hidden-import=openpyxl `
 --hidden-import=pandas `
 --hidden-import=geopy `
 --hidden-import=numpy `
 --hidden-import=datetime `
 --hidden-import=csv `
 --hidden-import=matplotlib `
 --collect-all openpyxl `
 .\the_python_script.py
