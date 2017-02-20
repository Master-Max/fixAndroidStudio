# fixAndroidStudio

http://android.stackexchange.com/questions/145437/reinstall-avd-on-ubuntu-16-04
  1.  $ sudo apt-get install lib64stdc++6 (if it is not installed)
  2.  $ cd ~/Android/Sdk/tools/lib64/libstdc++
  3.  $ mv libstdc++.so.6 libstdc++.so.6.original
  4.  $ ln -s /usr/lib64/libstdc++.so.6 ~/Android/Sdk/tools/lib64/libstdc++
  5.  $ sudo apt-get install mesa-utils (if it is not installed)

Basically Just Rename the file libstdc++.so.6 to libstdc++

  This file is found in /Android/Sdk/tools/lib64/libstdc++
  
Then run sudo apt-get install mesa-utils
  If it throws the error
    E: dpkg was interrupted, you must manually run 'sudo dpkg --configure -a' to correct the problem.
    
    Run: sudo dpkg --configure -a
    Then Run: sudo apt-get install -f mesa-utils //the -f is the "fix" modifier
