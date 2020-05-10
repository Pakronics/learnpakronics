# Python API for Third-Party Libraries

### `urequests` – Network Request Module <a id="urequests-&#x2013;-network-request-module"></a>

**Function**

`urequests.request(method, url, data=None, json=None, headers={})`  
Send a network request, it will block the response data returned to the network, parameters：

* _method_ method of establishing a network request. e.g. `HEAD`，`GET`，`POST`，`PUT`，`PATCH`, `DELETE`.
* _url_ URL of the network request.
* _data_ \(optional\), a dictionary, tuple list \[\(key, value\)\] \(will be form coded\), byte or class file object sent in the request body.
* _json_ \(optional\), json data sent in the request body.
* _headers_ \(optional\), HTTP header dictionary to be sent with the request.

`urequests.head(url, **kw)`  
Send a `HEAD` request, the return type is the response of the request, parameters：

* _url_ URL of the network request.
* \*\*kw request optional parameters.

`urequests.get(url, **kw)`  
Send a `GET` request, the return type is the response of the request, parameters：

* _url_ URL of the network request.
* \*\*kw request optional parameters.

`urequests.post(url, **kw)`  
Send a `POST` request, the return type is the response of the request, parameters：

* _url_ URL of the network request.
* \*\*kw request optional parameters.

`urequests.put(url, **kw)`  
Send a `PUT` request, the return type is the response of the request, parameters：

* _url_ URL of the network request.
* \*\*kw request optional parameters.

`urequests.patch(url, **kw)`  
Send a `PATCH` request, the return type is the response of the request, parameters：

* _url_ URL of the network request.
* \*\*kw request optional parameters.

`urequests.delete(url, **kw)`  
Send a `DELETE`request, the return type is the response of the request, parameters：

* _url_ URL of the network request.
* \*\*kw request optional parameters.

**Sample Code:**

```text
import codey
import urequests as requests
import time

# Fill in your router's ssid and password here.
codey.wifi.start('wifi_ssid', 'password')
codey.led.show(0,0,0)
while True:
    if codey.wifi.is_connected():
        codey.led.show(0,0,255)
        res = requests.get(url='http://www.baidu.com/')
        print(res.text)
        time.sleep(3)
    else:
        codey.led.show(0,0,0)
```

**Sample Code:2**

```text
import codey
import urequests as requests
import time

# Fill in your router's ssid and password here.
codey.wifi.start('wifi_ssid', 'password')
codey.led.show(0,0,0)
hour = minite = second = "00"
while True:
    if codey.wifi.is_connected():
        try:
            res = requests.get(url = 'http://www.time.ac.cn/timeflash.asp?user=flash').text
            hour_begin = res.find('<hour>') + len('<hour>')
            hour_end = res.find('</hour>')
            minite_begin = res.find('<minite>') + len('<minite>')
            minite_end = res.find('</minite>')
            second_begin = res.find('<second>') + len('<second>')
            second_end = res.find('</second>')
            if hour_begin > len('<hour>') and hour_end > hour_begin and \
               minite_begin > len('<minite>') and minite_end > minite_begin and \
               second_begin > len('<second>') and second_end > second_begin:

                if hour_end - hour_begin == 1:
                    hour = '0' + res[hour_begin:hour_end]
                elif hour_end - hour_begin == 2:
                    hour = res[hour_begin:hour_end]

                if minite_end - minite_begin == 1:
                    minite = '0' + res[minite_begin:minite_end]
                elif minite_end - minite_begin == 2:
                    minite = res[minite_begin:minite_end]

                if second_end - second_begin == 1:
                    second = '0' + res[second_begin:second_end]
                elif second_end - second_begin == 2:
                    second = res[second_begin:second_end]

                print(hour + ":" + minite + ":" + second)
                cur_time = hour + ':' + minite;
                codey.display.show(cur_time)
        except:
            print("get error data")
    else:
        codey.led.show(0,0,0)
```

**Sample Code:3**

```text
import codey
import urequests as requests
import ujson

# user_account and password is mblock's account and password
def get_user_request_header():
    post_data = ujson.dumps({ 'account': 'user_account', 'password': 'password'})
    request_url = 'http://passport2.makeblock.com/v1/user/login'
    res = requests.post(request_url, headers = {'content-type': 'application/json'}, data = post_data).json()
    header_data = ''
    if res['code'] == 0:
        header_data = { "content-type": 'application/json; charset=utf-8', "devicetype": '1'}
        header_data["uid"] = str(res['data']['user']['uid'])
        header_data["deviceid"] = '30AEA427EC60'
    return header_data

# Get weather information
# cid: checkpoint id
# arg: Information to be queried
#            aqi:  Air Quality Index
#            pm25: PM2.5 concentration
#            pm10: PM10 concentration
#            co:   Carbon monoxide concentration
#            so2:  Sulfur dioxide concentration
#            no2:  Nitrogen dioxide concentration
def get_air_quality_info(cid, arg):
    if not codey.wifi.is_connected():
        return ''
    post_data = ujson.dumps({ "cid": cid, "arg": arg})
    request_url = 'http://msapi.passport3.makeblock.com/' + 'air/getone'
    res = requests.post(request_url, headers = get_user_request_header(), data = post_data)
    text = res.text
    return float(text)

# Fill in your router's ssid and password here.
codey.wifi.start('wifi_ssid', 'password')
codey.led.show(0,0,0)
while True:
    if codey.wifi.is_connected():
        codey.led.show(0,0,255)
        data = get_air_quality_info('1539','aqi')  #1539 is Shenzhen checkpoint id
        codey.display.show(data)
    else:
        codey.led.show(0,0,0)
```

### `mqtt` – Message Queue Telemetry Transmission <a id="mqtt-&#x2013;-message-queue-telemetry-transmission"></a>

**Class**

`class mqtt.MQTTClient(client_id, server, port=0, user=None, password=None, keepalive=0, ssl=False, ssl_params={})` Instantiating the interface object of MQTT client, parameters：

* _client\_id_ the unique client id string used when connecting to the broker. If client\_id is zero length or None, then one will be randomly generated. In this case, the parameter `clean_session` of the `connect` function must be `True`.
* _server_ The host name or IP address of the remote server.
* _port_ \(optional\), the network port of the server host to connect to. The default port number is 1883. Please note that the default port number of the MQTT over SSL/TLS is 8833.
* _user_ \(optional\), the username registered on the server.
* _password_ \(optional\), the password registered on the server.
* _keepalive_ \(optional\), the client’s keepalive time out value. Default is 60 s.
* _ssl_ \(optional\), whether enable the SSL/TLS support.
* _ssl\_params_ \(optional\), SSL/TLS parameter.

`connect(clean_session=True)`  
Connect the client to the server, this is a blocking function, parameters：

* _clean\_session_ a boolean that determines the client type. If `True`, the broker will remove all information about this client when it disconnects. If `False`, the client is a durable client and subscription information and queued messages will be retained when the client disconnects.

`reconnect()`  
Reconnect to the server using the details provided previously. You must call `connect` before calling this function.

`disconnect()`  
Disconnect from the server.

`ping()`  
Test the connectivity between the server and client.

`set_last_will(topic, msg, retain=False, qos=0)`  
Set the will to be sent to the server. If the client disconnects without calling `disconnect()`, the server will post a message on its behalf, parameters：

* _topic_ The topic of the will post.
* _msg_ A will message to send.
* _retain_ If set to `True`, the will message will be set to the last known `good/reserved message` for the topic.
* _qos_ Is used for the quality of service level of the will.

`publish(topic, msg, retain=False, qos=0)`  
A message is sent from the client to the agent and then sent from the agent to any client that subscribes to the matching topic, parameters：

* _topic_ The topic of the message should be posted.
* _msg_ The actual message to send.
* _retain_ If set to True, the will message will be set to the last known `good/reserved message` for the topic.
* _qos_ The level of quality of service to use.

`subscribe(topic, qos=0)`  
Subscribe to a topic of the service, this module provides some helper functions to subscribe and process messages directly. For example `set_callback`, parameters：

* _topic_ The subject of the message to subscribe.
* _qos_ The level of quality of service to use.

`set_callback(f)`  
Sets the callback function for the topic subscription, which is called when the server responds to our subscription request, parameters：

* _f_ callback function.

`wait_msg()`  
Wait for the server until the server has no pending messages. This function is a blocking function.

`check_msg()`  
Check if the server has pending messages. If not, return directly, if any, do same processing as function wait\_msg.

**Sample Code:**

```text
from mqtt import MQTTClient
import codey
import time

MQTTHOST = "mq.makeblock.com"
MQTTPORT = 1883

# Fill in as you like
client_id = "20180911203800"

# Example Path
Topic = "/sensors/temperature/#"

mqttClient = MQTTClient(client_id, MQTTHOST, port=MQTTPORT, user='test', password='test', keepalive=0, ssl=False)

# Connect to the MQTT server
def on_mqtt_connect():
    mqttClient.connect()

# publish a message
def on_publish(topic, payload, retain=False, qos = 0):
    mqttClient.publish(topic, payload, retain, qos)

# message processing function
def on_message_come(topic, msg):
    print(topic + " " + ":" + str(msg))
    codey.display.show(msg)

# subscribe message
def on_subscribe():
    mqttClient.set_callback(on_message_come)
    mqttClient.subscribe(Topic, qos = 1)

# Fill in your router's ssid and password here.
codey.wifi.start('wifi_ssid', 'password')
codey.led.show(0,0,0)
codey.display.show(0)
while True:
    if codey.wifi.is_connected():
        on_mqtt_connect()
        on_subscribe()
        codey.led.show(0,0,255)
        while True:
            # Blocking wait for message
            on_publish("/sensors/temperature/home", str(38), qos = 1)
            mqttClient.wait_msg()
            time.sleep(1)
    else:
        codey.led.show(0,0,0)
```

