# nikke-auto
* All nature action, no need root
 - Android device 
 - ![alt text](next.png)



```java

#All nature action, no need root
#this script need android device, and enable developer mode.

#when developer mode ok then install android adb tool(for send device tap command)
brew install adb-enhanced

#image tool: imagemagick (for check blue button)
brew install imagemagick

# this is for unlimited tower automation
# script will chekc if blue "NEXT" the click it to next level

#change the xy 860 2200 as your device. (mine is S23U)
```

```shell
#!/bin/bash
adb shell input tap 860 2200;
while true; do
  adb exec-out screencap -p > screenshot.png
  magick screenshot.png -crop 5x5+860+2200 output.jpg
#  magick identify -verbose output.jpg | grep 'blue primary:' | awk -F'[(),]' '{print $2, $3, $4}'
  color=$(magick identify -format "%[pixel:u.p{1,1}]" output.jpg  |  awk -F'[(),]' '{print $4}')
  echo "Checking screen color..."
  if (( $(echo "$color > 180" | bc -l) )); then
    adb shell input tap 860 2200
  else
    echo "Not blue, value: $color"
  fi
  sleep 1;
done
```