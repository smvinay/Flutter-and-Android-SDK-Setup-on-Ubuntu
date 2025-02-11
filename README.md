# Flutter and Android SDK Setup on Ubuntu

## Install Flutter using Snap

sudo snap install flutter --classic


## Create a New Flutter Project

flutter create my_flutter_app
cd my_flutter_app


## Run and Build Flutter Application

flutter run
flutter build apk


## Install Android SDK and Command Line Tools
### Check if `sdkmanager` is Installed

which sdkmanager


### If Not Installed, Install Required Packages

sudo apt install apksigner -y
sudo apt install android-sdk-build-tools -y
sudo apt install google-android-cmdline-tools-11.0-installer -y


### Manually Install Android Command Line Tools

mkdir -p ~/Android/Sdk/cmdline-tools
cd ~/Android/Sdk/cmdline-tools

wget https://dl.google.com/android/repository/commandlinetools-linux-10406996_latest.zip
unzip commandlinetools-linux-10406996_latest.zip
rm commandlinetools-linux-10406996_latest.zip

mv cmdline-tools latest


## Set Environment Variables

export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$ANDROID_HOME/cmdline-tools/latest/bin:$ANDROID_HOME/platform-tools:$PATH
source ~/.bashrc


## Verify SDK Installation

sdkmanager --version


## Accept Android Licenses

flutter doctor --android-licenses


## Verify Flutter Setup

flutter doctor


---
This guide provides step-by-step instructions for setting up Flutter and the Android SDK on an Ubuntu system.

