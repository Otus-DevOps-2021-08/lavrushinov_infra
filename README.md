# lavrushinov_infra
lavrushinov Infra repository

Данные для подключения
bastion_IP 51.250.7.86
someinternalhost_IP 10.128.0.16
WEB-интерфейс pritunl: https://51.250.7.86

Для проброса ssh можно использовать alias:
  HostName 51.250.7.86
  Port 22
  User appuser
  IdentityFile ~/.ssh/appuser

Host someinternalhost
  HostName 10.128.0.16
  ProxyJump bastion
  Port 22
  User appuser
  IdentityFile ~/.ssh/appuser
  Подсмотрел в интернете