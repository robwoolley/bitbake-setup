# bitbake-setup

This repository adjusts the bitbake repository to package the
bitbake-setup tool into PyPI.


Clone the bitbake repository
```
git clone https://github.com/openembedded/bitbake.git src/bitbake
```

Copy the bitbake libraries. No changes made to bitbake/lib/bb after the copy.
```
cp -r bitbake/lib/bb src/bb
```

Create a bitbake_setup directory. No changes are made to __main__.py.
```
mkdir src/bitbake_setup
touch src/bitbake_setup/__init__.py
cp src/bitbake/bin/bitbake-setup src/bitbake_setup/__main__.py
```

Copy the bs4 library to package it and make it visible at execution.
No changes are made to bs4.
```
cp -r src/bitbake/lib/bs4 src/bs4
```

Copy the codegen.py module to package it and make it visible at
execution. No changes are made to codegen.py.
```
cp src/bitbake/lib/codegen.py src/
```

Copy the ply lirbary to package it and make it visible at execution.
No changes are made to ply.
```
cp -r src/bitbake/lib/ply src/ply
```
