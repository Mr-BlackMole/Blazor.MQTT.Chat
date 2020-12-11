# Blazor.MQTT.Chat
A Blazor (Client-side) chat application using MQTT with RabbitMQ and Paho Javascript library.

# Read the full article
https://talkdotnet.wordpress.com/2019/05/24/blazor-rabbitmq-and-mqtt-using-paho-with-jsinterop/

Step 1: Installing and configuring RabbitMQ

Go to the RabbitMQ website and download the latest version of RabbitMQ (version 3.7.15 at the time of writing). You will also need Erlang (version 22.0 at time of writing) as it’s a prerequisite for RabbitMQ.

Once you’ve installed Erlang and RabbitMQ you will need to enable the following plugins. To do this, follow the information on the RabbitMQ plugins page on their website about enabling plugins.

rabbitmq_management
rabbitmq_web_mqtt
If you are running windows you can search for the “RabbitMQ Command Prompt (sbin dir) shortcut under your start menu or you can navigate to the following folder in command prompt running as an administrator.

C:\Program Files\RabbitMQ Server\rabbitmq_server-x.y.z\sbin>

Run the following commands:


rabbitmq-plugins enable rabbitmq_management

rabbitmq-plugins enable rabbitmq_web_mqtt

Once you have enabled the plugins you can navigate to the management page by going to http://localhost:15672 if you have not changed the default port.

Default credentials:

username: guest

password: guest

What you want to make sure of is that the plugin has been enabled and a listening port has been setup. My RabbitMQ MQTT port is using the default MQTT port of 15675 as shown below.
