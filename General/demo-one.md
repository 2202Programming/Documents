# Creating a Robot

Before we get started actually programmin we have to get a project set up in eclipse. If you don't have Eclipse and all the FRC extensions installed on your machine yet go [here](/programming.md) to do that and pick this guide back up later. But if you do the setup is quite simple.

Basicly all you have to do to create the project is click file->new->project, then select the FRC robot in the wizard and give it a relevant name and make sure to select Iterative Robot. I choose miniature-enigma for the name of my project.

![New Project](/assets/Capture.PNG)

![](/assets/ProjectType.PNG)

![](/assets/Capture2.PNG)

# First Program

Now you have a fully working robot good job! For right now it does not do much, however it does look pretty. The code that eclipse generates is a little more advanced then we are now. So just strip out everything it generates but leave the methods, those are important.

If you removed everything correctly then it should look something like this.

``` java
package org.usfirst.frc.team2202.robot;

import edu.wpi.first.wpilibj.IterativeRobot;

/**
 * The VM is configured to automatically run this class, and to call the
 * functions corresponding to each mode, as described in the IterativeRobot
 * documentation. If you change the name of this class or the package after
 * creating this project, you must also update the manifest file in the resource
 * directory.
 */
public class Robot extends IterativeRobot {

 /**
 * This function is run when the robot is first started up and should be
 * used for any initialization code.
 */
 public void robotInit() {

 }

 /**
 * This function is called at the start of the autonomous section
 */
 public void autonomousInit() {

 }

 /**
 * This function is called periodically during autonomous
 */
 public void autonomousPeriodic() {

 }

 /**
 * This function is called periodically during operator control
 */
 public void teleopPeriodic() {
 }
}
```

This is a good start, but now lets add some functionality. Lets start by driveing a motor to values sent from the smartdashboard program. This execise demonstates two of the most common things you will do. 