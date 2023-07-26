# Report Log

## Entry 1 (21/06/2023) 

### (Solved)1. CNOT gate issue
[![img1](https://raw.githubusercontent.com/Unexpecteddonuts/project_report/main/Cnot%20issue%2C%20when%20move%20website%20breaks.png "img1")](https://raw.githubusercontent.com/Unexpecteddonuts/project_report/main/Cnot%20issue%2C%20when%20move%20website%20breaks.png "img1")
#### Discription
When the target qubit for the CNOT gate is changed and then its tried to move, or if the element is moved out of the box while dragging to a different pair of qubits it breaks the website in some instances.
#### Recomendation
Its difficult to say anything without looking at the code but its most possibly due to incorrect validation and error handling of the `drag`  related events.

### 2. Errors while altering the existing circuit before saving it.
![](https://github.com/Unexpecteddonuts/project_report/blob/main/bell%20state.png?raw=true)

#### Discription
for example in the above bell state circuit, if i were to ass another element after i click on the `simulator` button and then i add another CNOT with `q[2]`  as the target qubit and then take a measurement it the website hangs in some instances, this instance is one example.

#### Recomendation
This is due to some other elements conflicting in the event handling as this is not a consistent error. i tried 5 circuits and this error was seen twice.

### (solved)3. Simulating and Saving errors are very common.
![](https://github.com/Unexpecteddonuts/project_report/blob/main/cant%20save,%20cant%20simlate,%20errors%20very%20often.png?raw=true)
#### Discription
This is a problem that occurs very often and very often the website becomes unresponsive after a failed `simulator` task.

Another issue is the fact that if i shift between the `Circuit Composer` and the `Dashboard` to check on submitted `tasks` the `task` im working on in the composer gets cleared.

#### Recomendation
Unsaved `Circuit Composer` should be stored in the session data and not cleared with every tab change.

## Entry 2 (22/06/2023)

### Overview.
Fewer bugs were found today than yesterday.

### 1. QASM to Circuit 

#### Discription.
As the current interface stands there is no way a QASM circuit code can be concerted to a Circuit on the`Composer` and only after a successfull job do you get the QASM code foor your Circuit.

### (Solved)2. Editing Saved Circuit Bug Fixed

#### Discription.
 The buggy part where more qubits couldnt be added to a saved circuit has been fixed, i tried that today morning and it worked fine.
