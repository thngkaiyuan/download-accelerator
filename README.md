# Download Accelerator
A really simple download accelerator written in Python that uses [multi-part downloading](https://www.quora.com/How-does-IDM-internet-download-manager-work) to speed up your downloads.

## Usage
1. Configure in `dl_man.py`:
  1. The number of connections (e.g. `conns = 8`)
  2. Your temporary download directory (e.g. `tmp_dir = '/tmp/'`, to store the file parts)
  3. Your final download directory (e.g. `dl_dir = '/home/ubuntu/'`, to store the combined file)
2. Pass your URL as a parameter to the script as follows:
```
$ python dl_man.py http://download.thinkbroadband.com/5MB.zip
Downloading /tmp/5MB.zip_7
Downloading /tmp/5MB.zip_3
Downloading /tmp/5MB.zip_2
Downloading /tmp/5MB.zip_1
Downloading /tmp/5MB.zip_4
Downloading /tmp/5MB.zip_0
Downloading /tmp/5MB.zip_5
Downloading /tmp/5MB.zip_6
Downloaded /tmp/5MB.zip_7
Downloaded /tmp/5MB.zip_2
Downloaded /tmp/5MB.zip_3
Downloaded /tmp/5MB.zip_0
Downloaded /tmp/5MB.zip_5
Downloaded /tmp/5MB.zip_1
Downloaded /tmp/5MB.zip_6
Downloaded /tmp/5MB.zip_4
All parts downloaded. Joining files...
Joining complete. File saved in /home/ubuntu/5MB.zip
```

Enjoy!
