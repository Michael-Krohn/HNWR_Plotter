# HNWR_Plotter
Setup the plotting script:
```
cmsrel CMSSW_9_4_4
cd CMSSW_9_4_4/src/
cmsenv
git clone https://github.com/Michael-Krohn/HNWR_Plotter.git -b Run2Legacy_v3__Default
```

After creating the txt file with all of the limits within it following the instructions from here: https://github.com/Michael-Krohn/HiggsAnalysis-CombinedLimit/tree/HNWR/v8.0.1/HNWR_13TeV/2016

Place the txt file in HNWR_Plotter/rootfiles/Run2Legacy_v3__Default/Limit/Asymptotic/2016/

And modify the HNWR_Plotter/src/Draw_Limits.C script so that the new txt input file is being used

To run the plotting script:
```
cd HNWR_Plotter/
bash -l
source setup.sh
root -l -b -q "src/Draw_Limit(2016)"
```

