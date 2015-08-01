#Executive Overview
WITS is a consortium of software that helps the user understand *why* the blizzard of files on their machines are there, as well as for ensuring the integrity of them.

##General Architecture

The WITS system is composed of the following elements:

**A WITS store**  This is a program/database whose purpose is to receive, store, and dispense the information that is collected about your ideas, files, and issues.  Other elements of WITS will communicate with the WITS store and it is responsible for persisting whatever data it needs (likely using a db.)

**A file-system inspector** on every monitored machine.  This agent will periodically crawl the file systems on a particular machine and send what it finds back to the WITS store.

**A file-system event monitor** on every monitored machine.  This agent will watch the file system for changes and immediately report them to the WITS store.

**The Idea Map.** This is a model of the ideas that all of these files are supposed to implement, with connections to the relevant files.  This is an inherently customized thing and is most likely implemented with code.

**The WITS event log.** As the above subsystems operate they will generate various “events” that ought to be brought to your attention.  WITS provides a means to accumulate and view these events until such time as you can do something about them.

This architecture is very general and there is a broad range of details left up to implementation details, such as programming language, communication protocol, and security.

##The Architecture- Digging Deeper##

In order for WITS to do its job it's going to need to have some executive program and a database containing information about the relevant files, ideas, issues, etc., hence the WITS store.

**File System Inspection**
A major part of this puzzle is collecting the information about the file systems.  WITS uses two important methods, each of which have a fatal flaw.

**The File-system Crawler.**   Although this component is very good at finding everything in a file-system, it's not very good at reacting quickly to changes.  Even a file-system of moderate size could easily have hundreds of thousands of files.  Even the most efficient possible process for enumeration over all of this would take substantial time and/or bring the system to its knees, computationally speaking.  So we use the file-system event monitor as well.

**The File-system Event Monitor.**  This component is very good at noticing any change in a file system, but is woefully deficient in finding the vast majority of the files that sit unchanging.  So we use the file-system crawler for that.

Together the crawler and the file-system event monitor give us thorough coverage and fast response to changing files.

**Idea Map**
Another major part of this puzzle is the Idea Map.  Now that we're creeping closer to a reference implementation it's time to reveal some details.  Practically speaking, the web of ideas that one has is potentially very complicated.  It's not likely to be feasible to represent this information using simple structures such as lists or trees, but will in fact require full-blown OO.  Java is a good language for this sort of thing and so that's what the reference implementation uses.  The Idea Map interacts with the WITS store such that all ideas and files are properly connected.  

**Event Log**
We need some means of summarizing everything of interest about WITS that you need to know.  For example, if a file is found that has no purpose, that information should be available to the event log.    
