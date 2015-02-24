Paddle faster
	List of things that one can tweak

Photo of nuclear reactor
	Things that went horribly wrong - what can we learn from them
	This is a therapy session :-)
	
Glassfish monitoring
	Audience show of hands question - something about monitoring
	Thread dump with blocked thread
	Thread dump of thread that owns the lock
	Lesson - 
		what does LOW mean
		complexity comes at a price
		or, wind resistance example
		
Identity theft (the image sucks)
	Database constraint violations in logs
	Integer spun around
	Lesson -
		your system will grow quicker than you think
		maybe chat about how easy we use third party libraries
		
Garbage collection
	Audience -
		How many have tuned garbage collection in Java
		How many of you have made it better
		How do you it was better :-)
	It is hard to tune GC when you have high memory churn
	Small heap - frequent collections
	Large heap - infrequent but people will die while it happens
	System with too large heap - swapping while GC
	Lesson -
		Understand app's memory patterns
		You may have to fix your app
		Experiment where no one can get hurt (do try this at home)
		Verbose GC logs
		
Virtualization
	What can we learn from this picture?  It is very hard to find a picture on virtualization :-)
	Load average example
	Audience show of hands - is this system busy?
	And what does it mean when the CPUs are virtual?
	Or, if those virtual CPUs are dynamically scaled?
	Lessons -
		It is hard to understand how your system is doing if you don't understand the tech it is running on
		
Glassfish transaction journal
	System slowing down
	Thread dump of blocked thread
	What went wrong here?
		Glassfish writes a transaction log to be able to complete transactions on a crash
		This log was on a file system where application logs were been written
		Since they were trying to solve a problem log levels were set high and lots of logs
		Slowing down the transaction log
	Lessons -
		Systems can share resources in mysterious ways
		
File handles
	System complete stopped
	Log fragment from broker - too many open files
	Listed all the open files - found it was the JVM leaking handles on "VM attach" (jconsole / jvisualvm)
	Metrics collector running on broker that broke it
	Lessons -
		Soak test *all* parts of your application - even the monitoring bits
	Find out the reference to this bug
		
Message queues
