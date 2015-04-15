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

And checkout this code:

git clone git@github.com:gzevi/TagAndProbe.git

