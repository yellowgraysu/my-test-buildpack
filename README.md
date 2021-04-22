# Heroku Buildpack for Flutter
![header]
Automate your deployments on Heroku easily.

## 🔨 Setup

#### Add this Buildpack in your Heroku app 
   In dashboard:
   
   You can copy the [link](https://github.com/diezep/heroku-buildpack-flutter) of this repository and paste it in buildpacks or write **diezep/flutter** and will be added automatically.
   
   In Heroku CLI:
   ```shellscript
   $ heroku buildpacks:set diezep/flutter -a <Heroku App name>
   ```

#### Optional

   You can add optional [environment variables](#-environment-variables) to customize the deployment of your project but nothing is required, all are optional.
  
## 🚧 Environment variables:

All variables were built following the structure **FLUTTER_VARNAME** to identified easily in Heroku configurations. If you want to use some variable, remember **use the structure** following to the variable.

| Variable |   Type  |   Default        |  Description
|----------|---------|------------------| -------------------|
| CLEANUP  | *boolean* |  <center>true</center> |Remove **uneccessary files** of your project after the compile. |
|  VERSION | <center>*string*</center> | *Last version in [stable channel](https://flutter.dev/docs/development/tools/sdk/releases?tab=linux).* | The **name of the version** you want to use to compile the project.
|  BUILD | <center>*string*</center> | <center>flutter build web --release --quiet</center> | Customize the **command to compile** the project.| 

### Set variable
   Example of setting CLEANUP var in Heroku CLI:
   ```shellscript
   $ heroku config:set FLUTTER_CLEANUP=true -a project-name
   ```
### Example

The next image is an example of setting environment variables following the structure mentioned above :

![example_use_in_variables](https://user-images.githubusercontent.com/38699812/89090700-42447c00-d36a-11ea-8148-84af7cddfa21.PNG)

<!-- TODO: ## 📌 LICENCE -->
<!-- TODO: ## 📌 CONTRIBUTE -->

## 📝 Final note
   This buildpack is unofficial that means i don't have any conection with Heroku or Google from Flutter developer team <!--Although I would like belonging to any of the two :D -->. This repository was made as a hobby, i'm always interested in learn new things, this is one demostration of that :)
   
Recently, [@ludwiktrammer](https://github.com/ludwiktrammer) developed a lighter version of this buildpack with some improvements, if you are having problems with size of project or you are using Heroku CI, i invite you to test it. [here's the repo](https://github.com/EE/heroku-buildpack-flutter-light)
