# NE(a)T HEALER 
###centralizes DDoS alarms from multiple colletors, and take decisions based on thresholds.

HEALER listens to FastNetMon and Plixer Scrutinizer notifications.
When alarms are received, it takes actions based on configured thresholds.

Configure thresholds for different stages (cleared,warning,possible_ddos,under_attack)
... expand

Setup actions for each stage (email, pagerduty, script)
... expand


##Starting up

1. `script/bootstrap`
2. Populate `.env` with a config
3. `script/start`

<br>
##Available functions

### query
GET /healer/v1/ddos/status => query DDoS status

GET /healer/v1/ddos/verify => query DDoS alarms details

GET /healer/v1/ddos/verify/brief => query DDoS alarms brief

# post
POST /healer/v1/ddos/notify => post FastNetMon alarm