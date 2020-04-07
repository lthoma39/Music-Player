## Music-Player
Created a service for playing music

## Project Description 
Two Android apps. The first app, named ClipServer, stores a number of audio clips,
such as songs or other recordings. The clips are numbered 1 through n, where n is the total number of clips,
with n ≥ 5. This app contains a service intended to be both started and bound, which exposes an API
for clients to use. The API supports such functionality as playing one of the audio clips, pausing the clip,
resuming the clip and stopping the playback altogether. The ClipServer app includes at least 5 audio clips
of variable duration. The duration of Clip #1 should be at least 30 seconds but no more than 3 minutes.
Because ClipServer’s service has an effect on the user experience of the device, this service should run in
the foreground.
The second app, AudioClient consists of an activity that exposes functionality for using the ClipServer
and binds to the service for playing desired audio clips. AudioClient has the ability to start and stop the
service. Once the service is started, AudioClient allows an interactive user to play one of the n audio
segments. The AudioClient activity binds to the service for a duration of an audio clip. The activity unbinds
from the service when either a clip has ended or the user stops the playback; however, the service is not
stopped until the user decides to do so. (See UI spec below.) In other words, by default the service remains
in the started state even if it is not playing an audio clip
