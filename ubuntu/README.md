sudo docker run \
-v /srv/docker/ubuntu-python/enc/encrypt.py:/srv/encrypt.py \
-v /srv/docker/ubuntu-python/enc/mp4tools:/srv/mp4tools \
-v /srv/newDisk250Gb/media:/srv/files \
-v /srv/newDisk250Gb/output:/srv/output \
--cpu-quota="100000" \
--name enc1 \
-it ubuntupython_ubuntu bash

sudo docker exec -it python bash /srv/files/enc_script.sh

sudo docker exec -it enc1 bash /srv/files/00-script/enc1.sh
sudo docker exec -it enc2 bash /srv/files/00-script/enc2.sh
sudo docker exec -it enc3 bash /srv/files/00-script/enc3.sh
sudo docker exec -it enc4 bash /srv/files/00-script/enc4.sh
sudo docker exec -it enc5 bash /srv/files/00-script/enc5.sh
sudo docker exec -it enc6 bash /srv/files/00-script/enc6.sh
sudo docker exec -it enc7 bash /srv/files/00-script/enc7.sh
sudo docker exec -it enc8 bash /srv/files/00-script/enc8.sh
sudo docker exec -it enc9 bash /srv/files/00-script/enc9.sh
sudo docker exec -it enc10 bash /srv/files/00-script/enc10.sh



sudo docker exec -it python bash "/srv/encrypt.py --dir=/srv/files/new_enc --prod"
