---
description: Describes the steps of installing geometry gym plug-ins
---

# Installation

The steps below outline how to install the geometry gym plug-ins. For the majority of users, installation is simply a matter. However, sometimes you may need to manually replicate some of the steps of the installer \(particularly if you don’t have admin permissions\). If you have problems through the process please contact us.

An automated update may be possible in the near future.

## Before Installing 

Rhino plug-ins require Rhino to be installed and it is recommended that Grasshopper is also installed. Note v6 of Rhino now has Grasshopper built in.  

Revit plug-ins will require Revit to be installed

{% hint style="info" %}
Know which version of Rhino or Revit is installed on your computer. We currently provide installers for Rhino v5 and v6 and for all recent builds of Revit. If you cannot find the version that you require please contact us. 
{% endhint %}

You can download a trial version of the latest Rhino [here](https://www.rhino3d.com/download). 

## Step 1 - Download Installers

The latest Geometry Gym installer files can be downloaded from the downloads page \(.msi for Windows and .macrhi for Mac\):

#### [www.geometrygym.com/downloads](http://www.geometrygym.com/downloads) 

{% hint style="info" %}
It is highly recommend that **BullAnt** \(formerly known as StructDrawRhino\) is installed as a base as there are a lot of tools in which the other plug-ins rely on for streamlining workflows.
{% endhint %}

## Step 2 - Installing plug-ins

{% hint style="danger" %}
Make sure the Rhino or Revit application is not running prior to installing.
{% endhint %}

Find the installers from the folder that you selected at download.  

Run each of the installers by double clicking \(windows security might take a few seconds prior to permitting installation\).

The installer will attempt to create registry keys \(windows\) to instruct Rhino to load these plugins when starting. If you installed for the first time, Rhino should report loading of new plugins. When started, new rhino commands starting with gg such as ggGeodesicDome should be available.

If not and using Windows, the typical plugin installed location is C:\Program Files \(x86\)\Geometry Gym\Rhino3d Browse to this folder and drag and drop the .rhp files over the Rhino application window \(or load from rhino plugin manager\).

## Step 3 - Request Licence

You can read more about the Geometry Gym licencing system here:

{% page-ref page="licencing.md" %}



