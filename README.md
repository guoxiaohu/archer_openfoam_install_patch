# archer_openfoam_install_patch
ARCHER openfoam 5.x installation patch

In the HOME directory

mkdir $HOME/.modulefiles

copy PrgEnv-OpenFOAM-GNU to .modulefiles directory

echo "export MODULEPATH=$MODULEPATH:$HOME/.modulefiles" >> .profile

source .profile

The openfoam is installed in your work directory.

in your OpenFOAM-5.x

type:

git apply openfoam-5.x-archer.patch

and in Thirdparty directory

git apply thirdparty-5.x-archer.patch

then set up build env by

module swap PrgEnv-cray PrgEnv-OpenFOAM-GNU 
and source open etc/bashrc
