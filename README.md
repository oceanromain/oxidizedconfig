# oxidized install
##修改oxidized的UTC时间
opt/rh/rh-ruby23/root/usr/local/share/gems/gems/oxidized-web-0.13.1/lib/oxidized/web/public/scripts/oxidized.js

##配置
---
username: username
password: password
model: junos
resolve_dns: true
interval: 86400
use_syslog: false
debug: false
threads: 30
timeout: 20
retries: 3
prompt: !ruby/regexp /^([\w.@-]+[#>]\s?)$/
rest: 127.0.0.1:8888
next_adds_job: false
vars:
  remove_secret: true
groups: {}
models: {}
pid: "/root/.config/oxidized/pid"
crash:
  directory: "/root/.config/oxidized/crashes"
  hostnames: false
stats:
  history_size: 10
input:
  default: ssh, telnet
  debug: false
  ssh:
    secure: false
  ftp:
    passive: true
  utf8_encoded: true
output:
  default: git
  git:
    user: oceanromain
    email: starinternet@163.com
    repo: "/data/config.git"
hooks:
  push_to_remote:
    type: githubrepo
    events: [post_store]
    remote_repo: git@github.com:oceanromain/config.git
    publickey: /root/.config/oxidized/.ssh/id_rsa.pub
    privatekey: /root/.config/oxidized/.ssh/id_rsa 
source:
  default: csv
  csv:
    file: "/root/.config/oxidized/router.db"
    delimiter: !ruby/regexp /:/
    map:
      name: 0
      model: 1
      ip: 2
      username: 3
      password: 4
model_map:
  juniper: junos
  cisco: ios
  
##router.db
4507a:ios:192.168.88.10:kangpan:Aimer1982
4507b:ios:192.168.88.9:kangpan:Aimer1982
a1_01:ios:192.168.88.112:kangpan:Aimer1982
a2_01:ios:192.168.88.121:kangpan:Aimer1982
a2_02:ios:192.168.88.122:kangpan:Aimer1982
a2_03:ios:192.168.88.123:kangpan:Aimer1982
a2_04:ios:192.168.88.124:kangpan:Aimer1982
a2_05:ios:192.168.88.125:kangpan:Aimer1982
a2_06:ios:192.168.88.126:kangpan:Aimer1982
a2_07:ios:192.168.88.127:kangpan:Aimer1982
a3_01:ios:192.168.88.131:kangpan:Aimer1982
a3_02:ios:192.168.88.132:kangpan:Aimer1982
a3_03:ios:192.168.88.133:kangpan:Aimer1982
a3_04:ios:192.168.88.134:kangpan:Aimer1982
a4_01:ios:192.168.88.141:kangpan:Aimer1982
a4_02:ios:192.168.88.146:kangpan:Aimer1982
a4_hj1:ios:192.168.88.142:kangpan:Aimer1982
a4_hj2:ios:192.168.88.143:kangpan:Aimer1982
a4_hj3:ios:192.168.88.144:kangpan:Aimer1982
a5_01:ios:192.168.88.151:kangpan:Aimer1982
a5_02:ios:192.168.88.152:kangpan:Aimer1982
a5_03:ios:192.168.88.153:kangpan:Aimer1982
a5_04:ios:192.168.88.154:kangpan:Aimer1982
a5_05:ios:192.168.88.155:kangpan:Aimer1982
a5_06:ios:192.168.88.156:kangpan:Aimer1982
a5_07:ios:192.168.88.157:kangpan:Aimer1982
c10_01:ios:192.168.88.101:kangpan:Aimer1982
c1_01:ios:192.168.88.11:kangpan:Aimer1982
c4_01:ios:192.168.88.41:kangpan:Aimer1982
c4_02:ios:192.168.88.42:kangpan:Aimer1982
c5_01:ios:192.168.88.51:kangpan:Aimer1982
c5_02:ios:192.168.88.52:kangpan:Aimer1982
c5_03:ios:192.168.88.53:kangpan:Aimer1982
c6_01:ios:192.168.88.61:kangpan:Aimer1982
c6_02:ios:192.168.88.62:kangpan:Aimer1982
c6_03:ios:192.168.88.63:kangpan:Aimer1982
c7_01:ios:192.168.88.71:kangpan:Aimer1982
c7_02:ios:192.168.88.72:kangpan:Aimer1982
c7_03:ios:192.168.88.73:kangpan:Aimer1982
c8_01:ios:192.168.88.81:kangpan:Aimer1982
c8_02:ios:192.168.88.82:kangpan:Aimer1982
c9_01:ios:192.168.88.91:kangpan:Aimer1982
c9_02:ios:192.168.88.92:kangpan:Aimer1982
c9_03:ios:192.168.88.93:kangpan:Aimer1982
c9_04:ios:192.168.88.94:kangpan:Aimer1982
dc10:ios:10.2.1.87:kangpan:Aimer1982
dc12:ios:10.2.1.85:kangpan:Aimer1982
dc13:ios:10.2.1.84:kangpan:Aimer1982
dc14:ios:10.2.1.83:kangpan:Aimer1982
dc15:ios:10.2.1.82:kangpan:Aimer1982
dc16:ios:10.2.1.81:kangpan:Aimer1982
dc17:ios:10.2.1.80:kangpan:Aimer1982
hja4:ios:192.168.88.3:kangpan:Aimer1982
hjc5:ios:192.168.88.4:kangpan:Aimer1982
hjc7:ios:192.168.88.5:kangpan:Aimer1982
jifang-10:ios:192.168.88.254:kangpan:Aimer1982
jifang-11:ios:192.168.88.211:kangpan:Aimer1982
jifang-12:ios:192.168.88.212:kangpan:Aimer1982
jifang-13:ios:192.168.88.213:kangpan:Aimer1982
jifang-14:ios:192.168.88.214:kangpan:Aimer1982
jifang-16:ios:192.168.88.202:kangpan:Aimer1982
jifang-17:ios:192.168.88.200:kangpan:Aimer1982
jifang-18:ios:192.168.88.218:kangpan:Aimer1982
jifang-19:ios:192.168.88.219:kangpan:Aimer1982
jifang-2:ios:192.168.88.201:kangpan:Aimer1982
jifang-20:ios:192.168.88.220:kangpan:Aimer1982
jifang-21:ios:192.168.88.210:kangpan:Aimer1982
jifang-5:ios:192.168.88.205:kangpan:Aimer1982
jifang-6:ios:192.168.88.206:kangpan:Aimer1982
jifang-7:ios:192.168.88.207:kangpan:Aimer1982
jifang-9:ios:192.168.88.209:kangpan:Aimer1982
jifang-zm:ios:192.168.88.253:kangpan:Aimer1982
n9k1:nxos:10.2.1.100:kangpan:Aimer1982
n9k2:nxos:10.2.1.101:kangpan:Aimer1982
n9k3:nxos:10.2.1.102:kangpan:Aimer1982
n9k4:nxos:10.2.1.103:kangpan:Aimer1982
WFY:ios::ios:192.168.88.55:kangpan:Aimer1982
wifi1:ios:192.168.88.43:kangpan:Aimer1982
wifi2:ios:192.168.88.44:kangpan:Aimer1982
wifi3:ios:192.168.88.32:kangpan:Aimer1982
wifi4:ios:192.168.88.21:kangpan:Aimer1982
wifi5:ios:192.168.88.12:kangpan:Aimer1982
wifi7:ios:192.168.88.95:kangpan:Aimer1982
wiif6:ios:192.168.88.54:kangpan:Aimer1982
wifi8:ios:192.168.88.45:kangpan:Aimer1982
newct:ios:10.2.1.78:kangpan:Aimer1982
netcnc:ios:10.2.1.79:kangpan:Aimer1982
oldct:ios:192.168.88.251:kangpan:Aimer1982
oldcnc:ios:192.168.88.252:kangpan:Aimer1982
