# CONDA CHEATS ----------------------------------------------------------------------
* To clone an environment: conda create --name new_env_name --clone env_name_to_clone
* conda env list
* conda env remove --name <env>
* conda env create -f something.yaml
* conda create --name <env>
* conda env update --file something.yaml --prune

* pip install -r requirements.txt
* conda list -e > requirements.txt

# UBUNTU CHEATS --------------------------------------------------------------------
* Create txt File: cat > something.txt (Then click 'enter' write something and then ctrl+D)
## Convert jpeg to png
* find . -name "*.jpeg" -exec mogrify -format png {} \;
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
## Remove blank spaces
* rename "s/ *//g" *
## Replace spaces in file names with underscore
* rename 's/\s+/_/g' *
## Adding 'office_' to the name of the files
* rename 's/^/office_/' *
## Rename 'chessboard-R' with 'right' in names of files
* rename "s/chessboard-R/right/g" *

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
  
  
# OTHER CHEATS ----------------------------------------------------------------------
* Check the camera: v4l2-ctl --list-devices
* Disable Camera: sudo modprobe -r uvcvideo
* Enable Camera: sudo modporbe uvcvideo
