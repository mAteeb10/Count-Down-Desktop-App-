# Count Down Desktop-app
Countdown Timer using Threads and GUI
Introduction:
The "Countdown Timer" project aims to demonstrate the use of threads and graphical user interface (GUI) in Java. The project involves creating a simple GUI window with a label that displays a countdown from a specified number. The countdown runs in a separate thread while updating the GUI.
Objectives
•	Utilize Java's threading capabilities to run a countdown timer in the background while updating the GUI.
•	Create a graphical user interface (GUI) using Java Swing components to display the countdown.
•	Provide user interaction by starting the countdown when the application launches.
Project Components:
1. CountdownGUI Class
The CountdownGUI class is the main class of the project. It extends JFrame to create a GUI window with the following components:
JLabel: Displays the countdown value.
startCountdown() method: Starts the countdown by creating a new thread.
WorkerThread class: An inner class that extends Thread. It represents the background thread that performs the countdown.
2. WorkerThread Class
The WorkerThread class is an inner class of CountdownGUI and extends Thread. Inside the run method, it performs the countdown by iterating from a specified number to 0. It updates the countdownLabel using SwingUtilities.invokeLater() to ensure the update occurs on the Event Dispatch Thread (EDT). The thread sleeps for 1 second between each countdown step.
3. Main Method
The main method is used to initialize the CountdownGUI object and start the GUI. It uses SwingUtilities.invokeLater() to invoke the GUI creation on the EDT.

Implementation Steps:
1.	Create a new Java project in your favorite IDE.
2.	Implement the CountdownGUI class with the necessary components and the WorkerThread inner class.
3.	Test the application by launching it and observing the countdown label update every second.
Conclusion:
The "Countdown Timer" project successfully demonstrates the use of threads and GUI in Java to create a graphical application with a countdown timer. The project achieves the objectives by running the countdown in a separate thread while updating the GUI on the EDT. The user can start the countdown by launching the application.
Future Enhancements:
The project can be further improved by adding the following features:
1.	Allowing the user to input the initial countdown value.
2.	Implementing a pause and resume functionality for the countdown.
3.	Adding sound or visual effects when the countdown reaches 0.
4.	Providing options for different countdown formats, such as HH:MM:SS or MM:SS.
References:
•	Oracle Java Documentation: https://docs.oracle.com/javase/8/docs/api/
•	Java Swing Tutorial: https://docs.oracle.com/javase/tutorial/uiswing/
•	Stack Overflow: https://stackoverflow.com/ for various programming challenges and solutions.
