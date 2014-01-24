Assignment #0 log description 

Initially, when the app first starts up, the onCreate, onStart and onResume are called.
This is expected behavior as it follows the normal life cycle flow of the application. 
When the screen is rotated though, onPause, onStop and onDestroy are called. Then the 
onCreate, onStart and onResume are called again. The onRestart was never called as the activity 
was always destroyed and recreated on rotating the screen. 
This is most likely because the properties of the activity in landscape and portrait mode are different. 
The activity in landscape mode has different dimensions for the screen size and could have a different layout 
from the one in portrait mode. As a result on switching, the scheduler decides to shutdown the activity hence 
destroying it and recreate in afresh with it's new properties which might entail loading priorly unneeded resources

