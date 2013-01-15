pyircbot
========

A simple IRC bot interface written in Python 

Usage
-----
Easiest way to use is to put in the same folder as your own code, then use:

    import pyircbot
    from pyircbot import IrcEvent, IrcUser

### How to connect to a server:

	settings = { ... }
	bot = pyircbot.create(settings)
	bot.connect()

### Avaliable settings:

	settings = {
		'host': "pie-studios.com", 			# REQUIRED: a hostname or ip address to the IRC server
		'port': 6667, 						# REQUIRED: a port number to the IRC server
		'nick': "Nickname",					# REQUIRED: an IRC compliant nickname
		'ident': "pyircbot",					# REQUIRED: an IRC compliant ident
		'realname': "derp",					# OPTIONAL: a realname identifier
		'serverpassword': "xxpassxx",				# OPTIONAL: a password required to join the server, omit to skip
	}
	
	
### How to listen to events:

	import pyircbot
	from pyircbot import IrcEvent, IrcUser
	
	settings = { ... }
	def func(type, data):
		... # do stuff with event
	
	bot = pyircbot.create(settings)
	bot.RegisterEventHandler(IrcEvent.MessageRecieved, func)
	bot.connect()
	
### Available events:

	TODO
	
