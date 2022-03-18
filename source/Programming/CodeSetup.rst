##########
Code Setup
##########

Raid One Template
=================

Download the code from `here <https://github.com/TASRobotics/RaidOne-FRC-Template>`_ and open it
in WPIlib's VSCode. If random prompts pop up, use common sense and answer them.

.. note::
    Make sure that the code is not being backed up with Google Drive or Onedrive because it 
    screws things up. 

Installing Vendor Libraries
===========================

Ctrl + Shift + P --> Manage Vendor Libraries --> Install new libraries (offline) --> click the 
checkboxes

Configuring Motor Controllers & Sensors
=======================================

1. Update the firmware
2. Configure the CAN ID's of the motor controllers and sensors

How you might ask? RTFM (Read the Fun Manuals):
-----------------------------------------------

* `REV <https://docs.revrobotics.com/sparkmax/>`_
* `CTRE <https://docs.ctre-phoenix.com/en/stable/>`_

.. note::
    When configuring CAN ID's, you must do it 1 by 1 if they are new. Otherwise, the CAN 
    will think that all your devices are the same thing as they will be under the same 
    CAN ID. 

Top 5 ways of knowing you screwed up:
-------------------------------------

1. The CAN devices are blinking weird colors (probably a connection issue)
2. You can't see all your devices in Phoneix Tuner or the REV hardware client (probably also 
   a connection issue)
3. Phoenix Tuner thinks your Talon FX's are Talon SRX's (that's how you know your firmware is 
   way too old)
4. Only one devices shows up in Phoenix Tuner even though your CAN bus looks happy (this means 
   all your devices have the same ID)
5. You smell something burning (well that sucks)

Setting CAN ID's in Code
========================

Now that your CAN is happy, go to ``Constants.java`` and change the CAN ID's to match the ID's 
you set in the previous step. 