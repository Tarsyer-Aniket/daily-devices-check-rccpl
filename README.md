## RCCPL daily devices check
### daily devices sheet link
```
https://docs.google.com/spreadsheets/d/1i3NAV07JNxeJQIFseDmXCPqttTqfWbIdQlEZ6trUNdA/edit?usp=sharing
```

## Commands

### 1. htop check
#### Load average should not cross 3.5
```
htop
```

### 2. storage check
#### /tmp, root should not cross 50% of storage
```
df -h
```

### 3. temperature check
#### temperature should not cross 70
```
vcgencmd measure_temp
```

### 5. throttling check
#### Apart from throttled=0x0 should not come
```
vcgencmd get_throttled
```

## Service files status check
#### service file status should be Active and running
### 1. api_edge_device.service
```
systemctl --user status api_edge_device.service
```

### 2. camera_check.service
```
systemctl --user status camera_check.service
```

### 3. sending_loading_data.service
```
systemctl --user status sending_loading_data.service
```

### 4. heart_beat.service
```
systemctl --user status heart_beat.service
```

### 5. led_display.service
```
systemctl --user status led_display.service
```

### 6. tlm_bag_counting.service
```
systemctl --user status tlm_bag_counting.service
```

## Logs check
#### check date and time of recent logs, should not delay
### 1. led_display log
```
tail -f /tmp/led_display.log
```

### 2. heart_beat.log
```
tail -f /tmp/heart_beat.log
```

### 3. sending_loading_data.log
```
tail -f /tmp/sending_loading_data.log
```

### 4. processing logs
```
tail -f /tmp/sending_loading_data.log
```

## Dashboard check
#### check its updated for today, and last entry should be 1 hr before
```
https://lookerstudio.google.com/u/0/reporting/55a4477c-21c2-455e-88dd-e4d6c5c8cfd6/page/7rvlD
```


