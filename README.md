# AD2PN
An *Activity Diagram to Petri Net* model-to-model transformation realized with QVTo.

# Requirements:  
1. Eclipse
2. QVTo

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



