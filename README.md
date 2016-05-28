
#Title  
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.  

###Browser Matrix

| **OS**  | **OS Version**  |**Browser**| **Browser Version** | **Testing Type** |  
|---      |---              |---        |---                  |---               |  
|Windows  | 10              |  Edge     | 13+ (Latest)        | **Full**             |
|Windows  | -               |  IE       | 11                  | **Full**             |
| -       | -               | Firefox   | 44+ (Latest)        | **Full**             |  
| -       | -               | Chrome | 48+ (Latest)        | **Full**             |

###Mobile Matrix

| **Device**  | **OS**  | **OS Version**  |**Browser**| **Browser Version** | **Testing Type** |  
|---   |---   |---              |---        |---                  |---               |  
|IPhone       | IOS     |  9.2+           | Safari    | -|**Full** |
|IPad| IOS     |  9.2+           | Safari    | -|**Full** |
|Galaxy S6/ Edge| Android |  5.1.1           | Chrome | -|**Full** |
|Samsung S5| Android |  5.0+           | Chrome | -|**Full** | 


###Technologies Used  
Here is a list of the frameworks, libraries and tools used to build this project:  

####Front-end  

* AngularJS v1.0 ([link](example))   
* JQuery v2.0 ([link](example))  

####Back-end  

* Separate repo  ([link](example))  
  
####Build Tools  

* SASS v1.0 ([link](example))
* Grunt v1.0 ([link](example))

###Architecture  
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

##Getting Started  

###Prerequisites  
 You are going to need: 
  
 * Node  ([link](example))
 * Grunt-CLI   ([link](example))  
 * Bower  ([link](example))

####Environments  
This project has been built and tested on the following machines/systems: 

* Windows 10  
* Mac    

###Setup
1. clone repo  
2. open `cmd`  
3. `cd` into project folder  
4.  Run the following:  
 
 ```shell
 npm install  
 bower install
 ```

##Development

###Branches  
| **Branch**  | **Description**  |
|---      |---              |
|develop| This branch is used for stable development source code and will be used to compile code for staging.|
|staging| This branch is compiled code for staging servers. This code should be the compiled code from develop branch.|
|uat|This branch is compiled code QA.|
|master| This branch should be the source code deployed to the live environment. Do not merge into this branch unless you wish to deploy live.|
|release| This branch will have the compiled source code from the master branch and will be the code deployed to the live environment|

####Creating Branches  

Always create a branch from **develop**.

To create a **feature** branch, follow the naming convention below:
```
sprint-1/feature/feature-name
```  

To create a **bug** branch, follow the naming convention below:
```
sprint-1/bug/bug-name
```

###Launch Development mode

Run the following command to start developing and to stage the development environment

```shell
grunt dev
```

##Releasing Code
To release your code, use the following command:

```
grunt release [--prod || --uat]
```

###Flags
| **Name**  | **Description**  |  
|---   |---   |
|--uat| releases compiled code to the `uat` branch|  
|--prod| pushes development code to the `master` branch and releases compile to the `release` branch 

##API

###Component-1 Name
---
| **Property**  | **Description**  |  
|---   |---   |
|`getValue()`| returns a **String** value|
|`setValue(String:value)`| sets a **String** value|  

###Component-2 Name
---
| **Property**  | **Description**  |  
|---   |---   |
|`getValue()`| returns a **String** value|
|`setValue(String:value)`| sets a **String** value|