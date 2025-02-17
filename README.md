connect to euler by opening a new terminal/command prompt on your local machine and entering

*ssh yournethzname@euler.ethz.ch*

followed by your nethz password

make sure that you are in your personal home directory by

*pwd*

the output should read

*/cluster/home/yournethzname*


now clone this git repository into your home directory by

*git clone https://github.com/ecological-systems-design/test_euler.git*


now deploy the code on euler

*sbatch -n 4 --ntasks-per-node=2 --time=00:02:00 --mem-per-cpu=1g --wrap "python3 ./pi_scale_up_hpc.py"*