
#Title  

##Content  
[About](#About)  
----[Browser Matrix](#BrowserMatrix)  
----[Mobile Matrix](#MobileMatrix)  
----[Technologies Used](#TechnologiesUsed)  
----[Architecture](#Architecture)  
[Getting Started](#GettingStarted)  
----[Prerequisites](#Prerequisites)  
----[Setup](#Setup)  
[Development](#Development)    
----[Branches](#Branches)   
----[Launch Development Mode](#LaunchDevelopmentMode)    
----[Releasing Code](#ReleasingCode)   
[Usage](#Usage)   
----[API](#API)  

----------

##<a name="About"></a>About

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.  


###<a name="BrowserMatrix"></a>Browser Matrix

| **OS**  | **OS Version**  |**Browser**| **Browser Version** | **Testing Type** |  
|---      |---              |---        |---                  |---               |  
|Windows  | 10              |  Edge     | 13+ (Latest)        | **Full**             |
|Windows  | -               |  IE       | 11                  | **Full**             |
| -       | -               | Firefox   | 44+ (Latest)        | **Full**             |  
| -       | -               | Chrome | 48+ (Latest)        | **Full**             |

###<a name="MobileMatrix"></a>Mobile Matrix

| **Device**  | **OS**  | **OS Version**  |**Browser**| **Browser Version** | **Testing Type** |  
|---   |---   |---              |---        |---                  |---               |  
|IPhone       | IOS     |  9.2+           | Safari    | -|**Full** |
|IPad| IOS     |  9.2+           | Safari    | -|**Full** |
|Galaxy S6/ Edge| Android |  5.1.1           | Chrome | -|**Full** |
|Samsung S5| Android |  5.0+           | Chrome | -|**Full** | 


###<a name="TechnologiesUsed"></a>Technologies Used  
Here is a list of the frameworks, libraries and tools used to build this project:  

####Front-end  

* AngularJS v1.0 ([link](example))   
* JQuery v2.0 ([link](example))  

####Back-end  

* Separate repo  ([link](example))  
  
####Build Tools  

* SASS v1.0 ([link](example))
* Grunt v1.0 ([link](example))
* [vccp-dev](https://github.com/vccp/vccp-dev)

###<a name="Architecture"></a>Architecture  
Here is an overview of the project architecture:  

```
Core
  |- Theme
View
  |- MainView
    |- Template
    |- Style
    |- Controller
    
  |- SplashView
    |- Template
    |- Style
    |- Controller
Manager
  |- AssetManager
  |- SoundManager
Event
  |- EventDispatcher
```
 
Folder structure: 
 
```html
App/ <!-- Development source code-->
  |- src/ <!-- module and main files -->
    |- core/ <!--global files -->
    |- module-name/ <!-- module folder -->
      |- template/ <!-- module template files -->
      |- style/ <!-- module style files -->
      |- js/ <!-- module js files -->
  |- lib/ <!-- third-party library files -->
  |- resource/ <!-- resources for the app such as images and fonts -->
    |- image/ <!-- images -->
    |- font/ <!-- fonts -->
Dist/ <!-- Compiled code-->
Test/ <!-- Test scripts -->
Util/ <!-- for CLI -->
  |- task/ <!-- modules for a task runner such as grunt -->
  |- server/ <!-- node local server files -->
```

----------  

##<a name="GettingStarted"></a>Getting Started  

###<a name="Prerequisites"></a>Prerequisites  
 You are going to need: 
  
 * Node  ([link](example))
 * Grunt-CLI   ([link](example))  
 * Bower  ([link](example))  
 * [vccp-dev](https://github.com/vccp/vccp-dev)

####Environments  
This project has been built and tested on the following machines/systems: 

* Windows 10  
* Mac    

###<a name="Setup"></a>Setup
1. clone repo  
2. open `cmd`  
3. `cd` into project folder  
4.  Run the following:  
 
 ```shell
 npm install  
 bower install
 ```

----------

##<a name="Development"></a>Development

###<a name="Branches"></a>Branches  
| **Branch**  | **Description**  |
|---      |---              |
|develop| This branch is used for stable development source code and will be used to compile code for staging.|
|staging| This branch is compiled code for staging servers. This code should be the compiled code from develop branch.|
|uat|This branch is compiled code QA.|
|master| This branch should be the source code deployed to the live environment. Do not merge into this branch unless you wish to deploy live.|
|release| This branch will have the compiled source code from the master branch and will be the code deployed to the live environment|  
|documentation| This branch will be to store images and files for documentation|

####Creating Branches  

Always create a branch from **develop**.

To create a **feature** branch, follow the naming convention below:
```
sprint-1/feature/feature-name
```  

To create a **bug-fix** branch, follow the naming convention below:
```
sprint-1/bug-fix/bug-name
```

###<a name="LaunchDevelopmentMode"></a>Launch Development Mode

Run the following command to start developing and to stage the development environment

```shell
grunt dev
```

###Lint Your Code  

Please ensure all code is linted via the following command otherwise you cannot merge code to develop.  
```
vccp-dev lint
```

###Merging Code to Develop  

You should only use the following command when merging to the `develop` branch.  

```
vccp-dev merge-to-develop
```

----------

##<a name="ReleasingCode"></a>Releasing Code
To release your code, use the following command:

```
vccp-dev release [--prod || --uat]
```

###Flags  

Please read the documentation for [vccp-dev](https://github.com/vccp/vccp-dev).
| **Name**  | **Description**  |  
|---   |---   |
|--uat| releases compiled code to the `uat` branch|  
|--prod| pushes development code to the `master` branch and releases compile to the `release` branch. A **tag** will be created. |  
  
----------

##<a name="Usage"></a>Usage

###<a name="API"></a>API

####Component-1 Name
---
| **Property**  | **Description**  |  
|---   |---   |
|`getValue()`| returns a **String** value|
|`setValue(String:value)`| sets a **String** value|  

####Component-2 Name
---
| **Property**  | **Description**  |  
|---   |---   |
|`getValue()`| returns a **String** value|
|`setValue(String:value)`| sets a **String** value|