# retropie

For Raspberry run

sudo raspi-config > Advanced Options > GL Driver > G2 GL (Fake KMS) OpenGL desktop driver with fake KMS 

docker run -it --rm --name=retropieprova --privileged -e DISPLAY=unix$DISPLAY -e PULSE_SERVER=unix:/run/user/1000/pulse/native -v /run/user/1000:/run/user/1000 --group-add video -v /opt/vc:/opt/vc -v /var/run/dbus/:/var/run/dbus/ -v /dev/snd:/dev/snd -v /dev/input:/dev/input -v /dev/vchiq:/dev/vchiq -v /dev/vcio:/dev/vcio -v /dev/fb0:/dev/fb0 -v /dev/vcsm:/dev/vcsm lasery/retropie run
