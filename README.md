# Social-Force-Model
My Social Force Model simulation project! This code uses Python to model pedestrian movement with real data, visualized in Pygame, and analyzes forces and direction changes with Matplotlib. Check it out and tweak it to see how crowds behave!

A simple list I made of all the Python packages you need to install (like numpy and pygame) to get my code running. Just use `pip install -r requirements.txt` to set it up!

## Files Included
- `social_force_model.py`: The main Python script I wrote for this project. It runs the social force model simulation, handles agent movement with driving, agent, and wall forces, and includes Pygame visualization and Matplotlib plots for velocity and direction analysis. You’ll need to adjust the data path if your `real_data.csv` is in a different spot!
- `README.md`: This is my guide to the project! I put together instructions on how to run the simulation, what features it has, and some notes on using it. It’s written in Markdown so it looks nice on GitHub.
- `requirements.txt`: A simple list I made of all the Python packages you need to install (like numpy and pygame) to get my code running. Just use `pip install -r requirements.txt` to set it up!
- `real_data.csv`: My trajectory data file with pedestrian positions and velocities. It’s formatted for the code to work (columns: Track_ID, X, Y, Vx, Vy, Speed, Image_File). If you don’t have this, you’ll need to provide your own data and update the path in the script.
