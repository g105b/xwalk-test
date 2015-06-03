# xwalk-test
Just a test Crosswalk project

Install (apt-get): 

* python 
* ant 
* android-tools-adb
* android-tools-adbd

Test app (this repo)

```bash
# Create the containing directory
mkdir app && cd app
# Download the demo logo
wget https://crosswalk-project.org/assets/cw-app-icon.png icon.png -O icon.png
# Create the index.html and manifest.json
nano index.html manifest.json
# Build the APKs
python make_apk.py --package=org.crosswalkproject.example --manifest=../app/manifest.json --app-versionCode=1
# Put the APKs in the parent directory
mv *.apk ../.
```

Copy the apk to the device and locate it in the file manager to install.
