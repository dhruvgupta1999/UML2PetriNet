# AD2PN
An *Activity Diagram to Petri Net* model-to-model transformation realized with QVTo.

# Setup: installing Eclipse and QVTo
1. Download and install the Eclipse *Modeling* version (last tested with Eclipse 2018-12 on a Windows x64 machine) from https://www.eclipse.org/downloads/packages
2. Install **QVTo** (tested with v. 3.9.1) using the *update site*  http://download.eclipse.org/mmt/qvto/updates/releases/latest
3. Restart Eclipse when prompted


# How to transform an Activity Diagram to a Petri Net
Import the transformation projects (*AD2PetriNet* and *Common Utilities*) and the project containing the model (in .uml format) that you want to transform.
`Import > General > Existing Projects into Workspace`

Change to the *Java* perspective (using the icon on the top right corner of the window).

Select the transformation you want to run (for example AD2UPetriNetTransformation.qvto) and then select from the menu bar `Run > Transformation`.
1. Select the transformation (`AD2UPetriNet > transforms > AD2AD2UPetriNetTransformation.qvto`)
2. Select the input model (.uml) and choose where to save the output model (.xml)


## Optional Elements (UML editor)
The following packages are not required for performing the M2M transformation, but are suggested and provide a graphical editor for UML Diagrams.

### Sirius
More information: https://www.eclipse.org/sirius/

Check the latest version https://www.eclipse.org/sirius/download.html and select "Update Site", and, during the installation in Eclipse, **deselect all experimental packages!**

Update site (for v. 6.1.1 compatible with Eclipse 2018-12): http://download.eclipse.org/sirius/updates/releases/6.1.1/photon

### Acceleo
More information: https://www.eclipse.org/acceleo/

Update site: http://download.eclipse.org/acceleo/updates/releases/3.7
Packages: Acceleo, additional interpreters.

### UML Designer (Technische Universität Ilmenau's branch)
A modified version of the graphical tooling to edit and visualize UML models "UML Designer" (http://www.umldesigner.org/), released under the *EPL Open-Source License*. Its original source code is available on GitHub [here](https://github.com/ObeoNetwork/UML-Designer), whereas our modified code is currently available by sending a request to the Software and System Engineering department of the TU Ilmenau.

Update site: https://sse.tu-ilmenau.de/umldesigner-update
#### What are the differences between this branch and the original one?
#### Enhancements
- Support for Eclipse 2018-12
- Support for Sirius 6.1.0
- Added support for DataStore and CentralBuffer nodes

##### Fixes
- Remove the restriction for the operation selection during the CallOperationAction creation

##### Graphical Preferences
These changes make it easier to export diagrams in a higher quality format for black and white printing:
- The diagrams are displayed in black and white and icons are hidden
- Labels on control nodes are hidden by default
- Multiplicity from attributes has been hidden
- SVG representation of some nodes (e.g. final, initial nodes) instead of PNG
