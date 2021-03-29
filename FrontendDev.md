## Running kobo in developer mode.
1. Clone the latest version of [kobo-install](https://github.com/kobotoolbox/kobo-install).
2. Run the command ´python run.py´ to start the setup.
3. Enter the relevant information for the questions asked and just press enter if you don't want to change the default behaviour.
4. For the question ´Do you want to see advanced options?´, give the answer as ´Yes´ by typing 1.
5. For the question ´Use developer mode?´, give the answer as ´Yes´ by typing 1.
6. Then the setup will ask for the directories where it should clone KPI and KoboCat directories. For this step, create the relevant empty directories in a location and provide the path for these directories when asked for during the setup.(see Endnotes)
8. Now Kobo provides an option to run npm from inside the KPI container or locally wthin the KPI directory. Choose the relevant method to run the npm command. (For more information on running npm see Endnotes).
9. Then answer some more questions and the setup will complete. All the docker containers required for the kobo framework will be up and running.(see Endnotes)

### run `npm` from within the container
If you selected the option to run the npm in the container then you have to run  the following command in the terminal. 
```
./run.py -cf run --publish 3000:3000 kpi npm run watch
```
It will wait for any changes in the files in KPI and as soon as you make changes in the relevant files, the changes are pushed to the conatiner. Now the changes will be visible in the frontend.

### run `npm` locally from the filesystem

### Endnotes
1. The setup will clone KPI and KoboCat repositories in the directories provided. Edit the files here to make the changes in fronend.
2. npm is responsible for running the code(compiling, etc.). Visit [this](https://docs.npmjs.com/about-npm) for more information on npm.
