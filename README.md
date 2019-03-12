# QC8

```bash
scram p -n QC8Test CMSSW CMSSW_10_5_0_pre2
cd QC8Test/src
cmsenv
git-cms-merge-topic jshlee:gem-vfatv3
git clone -b Analyzer git@github.com:hyunyong/QC8.git
mv QC8/* .
rm -rf QC8
scram b -j 12
cd Analyzer/GEMQC8/test
cmsRun runGEMCosmicStand_data_test.py
```
