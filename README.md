We write this toolkit as a pre-process and post-process tools for vasp,named "Helpful VASP Usage Tools"(HVT)

Runing Environment(Linux x64 Bit),we have tested it on: (Platforms and Version)
Ubuntu >20.04 (need run "sudo dpkg-reconfigure dash" and choose "No") 
Centos >6.0
RedHat >5.0
We did not have tested it on Mac for no apple device.

The rest of the environmental requirements:
	Python 3.9 or higher
	Numpy 1.26.0 or higher
	Scipy 1.11.3 or higher
	matplotlib 3.0.1 or higher
	pymatgen 2023.10.4 or higher
	pymatgen-analysis-diffusion 2023.8.15 or higher
	ase 3.22.1 or higher
	pandas 1.3.4 or higher
If you need to use the full functionality of HVT, be sure to set up the above environment.

How to install it on your Linux system:
1.First you need to download the HVT installer from Github （https://github.com/Fakescode/HVT-toolkit）.
2.Place the HVT installation package in the installation folder of your server, run “tar -zxvf hvt.tar.gz” to extract the “hvt.tar.gz” file.
3.After completing the above steps a folder named “hvasptools” will be created, go to this folder，use the command “bash install.sh” to install HVT.
	Users can also add the following lines to the environment variable(e.g. .bashrc):
		export hvtpath=/home/your-account/hvt   #The path needs to be set according to the server environment you are using.
		export PATH=$hvtpath:$PATH
4.Download potential(POTCAR) files from https://www.vasp.at/ and exact in $hvtpath/bin/POTCAR accordingly.
5.Then users could relogin and use command "hvt" to get the help document.

Files architecture of HVT:
$hvtpath/bin/INCAR: INCAR templates, users can change it according to their needs.
$hvtpath/bin/KPOINTS: Scripts used to generate KPOINTS file.
$hvtpath/bin/POSCAR: Scripts used to preprocessing POSCAR file.
$hvtpath/bin/POTCAR: Scripts used to preprocessing POTCAR file.
$hvtpath/source-code: the original code for other tools for pre-process and post-process.
$hvtpath/addscripts:Users can place their code in this folder and later call it from any location.

Admittedly, there is still further development to be done on this software, so stay tuned!

Good Lucky!

