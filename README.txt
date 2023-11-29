This Repository contains code for performing active learning in Diffusion solver setting. The data can be generated using the code at this link "https://github.com/jquetzalcoatl/DiffSolver".

After generating the simulation data for training store them in a location (E.G. PATH_TO_DATA) and update the code run.py and loaders.py with the path (PATH_TO_DATA)

IMPORTANT CODE VERSIONS
Python 		3.11.4
PyTorch		2.0.1
numpy 		1.25.0
matplotlib 	3.7.1

Other libraries used
time
os
csv
copy



Running the code (example)
python run.py --net unetab --es 1 --func entropy --sub std  --card 3
-> --net = Surrogate network (unetab or simplecnn)
-> --es stands for early stop
-> --func = Acquisition function (entropy, diversity, tod, random)
-> --sub = Subset of entropy acquisition function (loss or std)
-> --card = Which GPU to run the code in