# Social Force Model Simulation

This is my Python project simulating pedestrian movement using the Social Force Model. It all started with my initial experiments, which I explored and presented in a PowerPoint for class—those are the roots of this code! I’ve built it to work with real trajectory data, visualize agent movements with Pygame, and analyze forces and direction changes using Matplotlib. The code here reflects those early ideas, and I’ve since come up with an updated method to improve the framework, detailed in the `Methodology of SF experiments.md` file. Check out `Initial_SF_Experiments.pptx` to see where it all began!

## Features
- Simulates how pedestrians move based on social forces.
- Shows trajectories with a cool Pygame visualization.
- Calculates average forces and direction changes for analysis.

## Files Included
- `social_force_model.py`: The main Python script I wrote for this project. It runs the social force model simulation, handles agent movement with driving, agent, and wall forces, and includes Pygame visualization and Matplotlib plots for velocity and direction analysis. You’ll need to adjust the data path if your `real_data.csv` is in a different spot!
- `README.md`: This is my guide to the project! I put together instructions on how to run the simulation, what features it has, and some notes on using it. It’s written in Markdown so it looks nice on GitHub.
- `requirements.txt`: A simple list I made of all the Python packages you need to install (like numpy and pygame) to get my code running. Just use `pip install -r requirements.txt` to set it up!
- `real_data.csv`: My trajectory data file with pedestrian positions and velocities. It’s formatted for the code to work (columns: Track_ID, X, Y, Vx, Vy, Speed, Image_File). If you don’t have this, you’ll need to provide your own data and update the path in the script.
- `Methodology of SF experiments.md`: This file explains my updated approach to the Social Force Model framework. I wrote down how I plan to tweak the parameters and methods to get better simulation results.
- `Initial_SF_Experiments.pptx`: The PowerPoint presentation I made for class where I first shared my experiments with the Social Force Model. It has the early ideas and results that led to this code.

## Notes
- The `real_data.csv` file needs to be in the right spot (e.g., `E:\DOWNLOAD\real_data.csv` as coded, or adjust the path).
- Feel free to tweak the constants like `SCALE` or `DRIVING_FORCE_TAU` to see different behaviors!
