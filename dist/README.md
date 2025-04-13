# Building the app


If the app needs to be rebuilt, run these:

1. Create the environment with all the dependencies:
```
conda env create -f environment.yml
```


2. Delete any previous builds:
```
rm -rf build dist dosimetry_app.spec
```


3. Build and package the app:
```
pyinstaller ./dosimetry_app.py --windowed --onefile \
  --hidden-import=numpy \
  --hidden-import=pandas \
  --hidden-import=matplotlib \
  --hidden-import=scipy \
  --hidden-import=scipy.signal \
  --hidden-import=soundfile \
  --hidden-import=parselmouth \
  --hidden-import=tkinter \
  --hidden-import=openpyxl
```
