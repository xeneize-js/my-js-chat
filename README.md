# Chat app written in node.js and socket.io

## Libraries used
<ul>
  <li>node.js / npm</li>
  <li>socket.io</li>
  <li>express</li>
  <li>node-uuid</li>
  <li>underscore</li>
  <li>ejs</li>
</ul>

# Functionality
<ul>
  <li>People are able to join the chat server after entering their names</li>
  <li>Usernames are unique - if a username is taken, a new suggestion is generated</li>
  <li>User agent and geo location are both detected</li>
  <li>People can setup a room. Room names are unique. One person can create on room and join one room</li>
  <li>Users have to join a room to chat, except for the whisper feature.</li>
  <li>Whisper messages are private messages sent between two users</li>
  <li>With a WebSpeech enabled browsers, users can record their messages</li>
  <li>Users can leave a room and/or disconnect from the server anytime</li>
  <li><strong>New:</strong> People joining the room will see the past 10 messages (chat history).</li>
  <li><strong>New:</strong> People will see an 'is typing' message when someone is typing a message.</li>
</ul>

## Setup and configuration

Make sure that you update <strong>server.js</strong>:
<pre>server.listen(app.get('port'), function(){
  console.log('Express server listening on port ' + app.get('port'));
});</pre>
and add your own IP address/hostname if required, i.e.:
<pre>server.listen(app.get('port'), "localhost", function(){
  console.log('Express server listening on port ' + app.get('port'));
});</pre>

(the port is defined in the <code>app.set('port', process.env.PORT || 3000);</code> section.)

Please also update <strong>public/js/client.js</strong>:
<pre>var socket = io.connect("localhost:3000");</pre>
with the right IP address/hostname.

To install <code>npm install && bower install</code> and to launch run <code>npm start</code>.

