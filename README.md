# Air-raspberry

Python script writing every hour the PM 2,5 & PM 10 using a Particulates sensor SDS011 on a raspberry 

The generated file (data.json) is used to create graphs https://github.com/Nairolf92/air-raspberry-graph

The generated data looks like this :

```
[{"pm10": 4.5, "pm25": 2.3, "time": "23/07/2019 13:55:16"}] 
```

## Background usage

If the script isn't launched through crontab (see next point) use this 

`python air.py`

ctrl +z

`bg "%python"`

 ## Crontab usage
 
In order to always get the data, even while the raspberry needs a reboot, add this:

`crontab -e`

`@reboot cd /home/user/air-raspberry && python air.py
`