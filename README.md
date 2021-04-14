# cimemctdriver
Repo containing the code from cime/src/drivers/mct.  Used only for moving from cime submodule to directory in E3SM.

How it was made:
git clone --no-tags git@github.com:ESMCI/cime.git   (Used hash f5433921b2d3330290773aa3553e5c5514ece3dc from April 10, 2021.)
cd cime
git filter-repo --path-rename driver_cpl:driver-mct src/mct/driver:driver-mct  (this takes the code in driver_cpl and its renamed path src/mct/driver and rewrites history so all files are in driver-mct)
git filter-repo --path driver-mct   (this removes all code except driver-mct leaving a commit history for just the code in driver-mct)
git remote add mctdriver (this repo)
git push mctdriver master


