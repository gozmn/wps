# wps
Install WPS Office in linux and issues fixed

1. Download WPS Office from https://www.wps.com/. You may choose Deb Package or Rpm Package accordingly.
2. Double click to install it in your GUI environment
3. Once you complete the installation, there are two potaincial issues to be fixed.
   1) Missing fonts issue
      
      Download all those fonts from <a href="missing_fonts">missing fonts</a> folder and copy them to the folder (/usr/share/fonts/wps-office or within /usr/share/fonts)
      
   3) Can not export to PDF issue
      
      $ cd /usr/lib/x86_64-linux-gnu <br>
      $ ls -l libtiff* <br>
      if there is nothing appeared, please install libtiff package, e.g., sudo apt install libtiffX (X is the version number, e.g., libtiff6) <br>
      $ sudo ln -s libtiff.so.6.0.0 libtiff.so.5 (replace 'libtiff.so.6.0.0' with your system one accordingly) <br>
