sudo docker run \
-v /srv/docker/ubuntu-python/enc/encrypt.py:/srv/encrypt.py \
-v /srv/docker/ubuntu-python/enc/mp4tools:/srv/mp4tools \
-v /srv/media:/srv/files \
-v /srv/output:/srv/output \
--cpu-quota="100000" \
-- name=enc
-it ubuntupython_ubuntu bash

sudo docker exec -it python bash /srv/files/enc_test.sh
sudo docker exec -it python bash "/srv/encrypt.py --dir=/srv/files/new_enc --prod"