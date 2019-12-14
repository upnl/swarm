유피넬 도커 스웜
========

```sh
# 도커가 기본값으로 IPv6를 지원하지 않아, localhost가 기본으로 ::1 를 가리키는
# 환경에선 문제가 있을 수 있다는 점에 유의하라
#
# Reference: https://docs.docker.com/v17.09/engine/userguide/networking/default_network/ipv6/

sudo git clone https://github.com/upnl/swarm.git /srv/swarm

sudo docker swarm init
sudo docker stack deploy -c /srv/swarm/gitlab.yml gitlab
```
