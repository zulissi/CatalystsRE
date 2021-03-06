# Catalysts for Renewable Energy

### Setup:
* Make sure you're in the project directory (`/CatalystsRE`)
* Install [Docker](https://www.docker.com/get-docker)
* Run  `docker build -t c4g .` to build the docker image.

### Run:
* Run `docker run -it -p 3000:3000 -p 9200:9200 --rm c4g /bin/bash -c "source /home/start.sh"` to start the server in a docker container. this command puts you inside the terminal that runs the script found in (`/CatalystsRE/start.sh`) and exposes the necessary ports to view the application in your browser. Ignore any error messages concerning connection with elasticsearch. (Node may not have given elastic enough time to start fully.)

* To see elasticsearch in your browser, it can be viewed at `localhost:9200`. Ensure that it works before continuing.

* Visit `localhost:3000/import` in your browser to populate elastic with example datapoints. This may be necessary for a graph to load.

* Finally, visit `localhost:3000` in your browser to view the application. Enjoy!

### Generating the json data file

* use `python lib/etc/import.py YYY.pkl` to generate the json file in the same place. This json file needs to go do sm1.cheme.cmu.edu:~/CatalystsRE/data/ to update the running instance. 

