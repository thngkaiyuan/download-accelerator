# Download Accelerator
**Download Accelerator** is a really simple (and did anybody mention free??!!?) download accelerator written in Python that uses [multi-part downloading](https://www.quora.com/How-does-IDM-internet-download-manager-work) to speed up your downloads. It even supports unstable connections by continuing where it left off if your connection is reset at any point of time. The only feature lacking is a real-time progress indicator but you don't really need it when your download is fast, right?

## Usage
1. Configure in `dl_man.py`:
  1. The default number of connections (e.g. `default_conns = 8`)
  2. Your temporary download directory (e.g. `tmp_dir = '/tmp/'`, to store the file parts)
  3. Your final download directory (e.g. `dl_dir = '/home/ubuntu/'`, to store the combined file)
2. Pass your URL as a parameter to the script as follows:

        $ python dlman.py http://download.thinkbroadband.com/1GB.zip
        Downloading part 6 to /tmp/1GB.zip_5
        Downloading part 4 to /tmp/1GB.zip_3
        Downloading part 1 to /tmp/1GB.zip_0
        Downloading part 5 to /tmp/1GB.zip_4
        Downloading part 7 to /tmp/1GB.zip_6
        Downloading part 3 to /tmp/1GB.zip_2
        Downloading part 2 to /tmp/1GB.zip_1
        Downloading part 8 to /tmp/1GB.zip_7
        Downloaded part 6 to /tmp/1GB.zip_5
        Downloaded part 4 to /tmp/1GB.zip_3
        Downloaded part 5 to /tmp/1GB.zip_4
        Downloaded part 1 to /tmp/1GB.zip_0
        Downloaded part 7 to /tmp/1GB.zip_6
        Downloaded part 2 to /tmp/1GB.zip_1
        Downloaded part 8 to /tmp/1GB.zip_7
        Downloaded part 3 to /tmp/1GB.zip_2
        All parts downloaded. Joining files...
        Joining complete. File saved in /home/ubuntu/1GB.zip

3. You can also pass in the number of connections (which will override the default) as a command line argument as follows:

        $ python dl_man.py http://download.thinkbroadband.com/5MB.zip 2
        Downloading part 2 to /tmp/5MB.zip_1
        Downloading part 1 to /tmp/5MB.zip_0
        Downloaded part 2 to /tmp/5MB.zip_1
        Downloaded part 1 to /tmp/5MB.zip_0
        All parts downloaded. Joining files...
        Joining complete. File saved in /home/ubuntu/5MB.zip

3. Enjoy!
