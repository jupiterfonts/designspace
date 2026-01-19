# This is a template. Change all of the information you need.
from fontTools.designspaceLib import DesignSpaceDocument, SourceDescriptor
import sys

# Replace these with the paths to your UFO files
ufo_paths = [
    # You need at least two UFO directories.
    # This should be your lightest font.
    "FONTFAMILY-Light.ufo",
    # This should be your normal font.
    "FONTFAMILY-Regular.ufo",
    # This should be your heaviest font.
    "FONTFAMILY-Black.ufo"
    # Add more UFO paths as needed. You can add more weights if you want.
]

# Create a new DesignSpace document
doc = DesignSpaceDocument()

for ufo_path in ufo_paths:
    source = SourceDescriptor()
    source.path = ufo_path
    source.name = ufo_path.split('/')[-1].replace('.ufo', '')
    source.location = {}  # Define the location in the design space axes
    doc.addSource(source)

# Define axes if necessary
# For example:
from fontTools.designspaceLib import AxisDescriptor
axis = AxisDescriptor()
axis.name = "Weight"
axis.tag = "wght"
axis.minimum = 400
axis.maximum = 900
axis.default = 400
doc.addAxis(axis)

# Save the DesignSpace document
doc.write("FONTFAMILY.designspace")
