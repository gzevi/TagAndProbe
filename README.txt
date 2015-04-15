# TagAndProbe

To set things up, first set up CMSSW:

export SCRAM_ARCH=slc6_amd64_gcc481
source /cvmfs/cms.cern.ch/cmsset_default.sh
cmsrel CMSSW_7_2_0
cd CMSSW_7_2_0/src
cmsenv

Then checkout Ryan's analysis tools:

git clone https://github.com/kelleyrw/AnalysisTools.git 
cd $CMSSW_BASE/src/AnalysisTools
git checkout tnp_V00-00-00
cd $CMSSW_BASE/src/

Checkout this code:

git clone git@github.com:gzevi/TagAndProbe.git

And compile!
scramv1 b -j10

To run the first step (plot making)
cd TagAndProbe/Analysis
tnp_make_plots config/ElectronID_2015test.py

For detailed instructions, look at Ryan's twiki, skipping the babymaking 
http://www.t2.ucsd.edu/tastwiki/bin/view/CMS/TagAndProbe#Calculate_the_Efficiency

Useful tool to remake LeptonTree.h/cc files after changing the LeptonTree
TagAndProbe/Analysis/tools/makeLeptonTreeClassFiles.sh

