This is the diagram for how the command runner runs in auto.

<img src="Pics/ClassDiagram.jpg" width="400px">

Some type of selection system (most likely smart dashboard) will choose StartPosition, Shoot or not, and cross the line or not. This chart
shows how we will handle these choices during auto.

<img src="Pics/DecisionChart.jpg" width="400px">

This is a reference for starting positions and paths.

<img src="Pics/ReferenceArena.jpg" width="400px">

This also shows that we will reverse all turns when on the opposite side of the field.

A simple flow for during auto.

<img src="Pics/Flow.jpg" width="400px">

During teleop, auto commands will be able to be called by using an auto command runner.
