# Hassio-broadlink_cover
broadlink_cover


////////////////////////////////////////////////////////////////////////////////////////////////

cover:
  - platform: broadlink_cover
    host: 192.168.10.XXX
    mac: '34:EA:34:E3:XX:XX'
    covers:
        bedroom_cover:               #///////无传感器设置
          name: "窗帘"                 
          travel_time: 8
          command_open: '############'
          command_close: '############'
          command_stop: '############'


////////////////////////////////////////////////////////////////////////////////////////////////

cover:
  - platform: broadlink_cover
    host: 192.168.10.XXX
    mac: '34:EA:34:E3:XX:XX'
    covers:        
        livingroom_cover:
          travel_time: 8
          position_sensor: binary_sensor.door_window_sensor #//////有传感器设置
          name: "窗户"
          command_open: '############'
          command_close: '############'
          command_stop: '############'
///////////////////////////////////////////////////////////////////////////////////////////////
