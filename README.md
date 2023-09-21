# emulator_testing


Melissa's repo for testing cmssw emulator output.

cmssw emulator repo: https://github.com/quinnanm/cmssw/tree/emulator_aug23
external hls4ml repo: https://github.com/cms-hls4ml/AXOL1TL
sioni's firmware repo: https://gitlab.cern.ch/ssummers/run3_ugt_ml/-/tree/axol1tl1_v2

instructions for setting up emulator cmssw can be found in cmssw repo readme

testfiles located here: /afs/cern.ch/user/m/mequinna/public/axol1tl_cmssw_emulator/

running the testfile: 

```
cmsDriver.py l1Ntuple -s RAW2DIGI --python_filename=data_def.py -n -1 --no_output --era=Run3 --data --conditions=130X_dataRun3_Prompt_v4 --customise=L1Trigger/Configuration/customiseSettings.L1TSettingsToCaloParams_2023_v0_3 --customise=L1Trigger/Configuration/customiseUtils.L1TGlobalMenuXML --customise=L1Trigger/Configuration/customiseReEmul.L1TReEmulFromRAW --customise=L1Trigger/L1TNtuples/customiseL1Ntuple.L1NtupleRAWEMU --filein=/store/data/Run2023C/JetMET0/RAW/v1/000/368/566/00000/81c206fd-f1d4-4f09-905b-4a185cf097c2.root --fileout=L1Ntuple.root >L1Ntuple_info.txt
```

setting up jupyter notebook environment:

```
# create a new conda environment
conda create -n rootstuff python=3.8
conda activate rootstuff
conda install jupyter


# install the necessary python packages
pip install numpy pandas scikit-learn scipy matplotlib tqdm PyYAML

# install uproot for reading/writing ROOT files
pip install uproot awkward

jupyter notebook


```
