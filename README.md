#Executive Overview
WITS is a consortium of software that helps the user understand *why* the blizzard of files on their machines are there, as well as for ensuring the integrity of them.

##Rationale
Within about one hour of my odyssey in dealing with computers started, commenced the problem of managing the collection of files and directories that infest them.  Whether I am dealing with a single machine or an entire flock of them, I want to know WITS!  Basically, for each file, I want to know why it's there.

The reason these files exist is because somebody has ideas that they want to implement.  Unfortunately some of these ideas are goals of other people, frequently with unsavory intent, such as marketers, spies, and hackers.   How can we collect and record the information about all these files and ideas, connect them together, and determine specific issues to deal with?   That is the challenge that the WITS consortium addresses.

The essence of the WITS solution is to build a database containing information about the various files and ideas involved, as well as their relationships.  These relationships come in all shapes and sizes and link the files and ideas together.

As the information about the files and ideas is discovered, organized, and clarified, certain issues will emerge.  These issues are specific things that ought to be done, such as determine the purpose of a specific file.  This is the foundation of providing the “why” for the existence of each file.  This step is somewhat easier said than done and we will encounter devils in the details as we develop this further.

WITS gives you the ability to ignore the details below a certain level in a file-system.  So for example your model might mention that “/etc” exists due to the idea of “My Ubuntu installation” while ignoring the blizzard of details within.  With WITS you can quickly outline the forest, but refine your view of the trees at your leisure.

Once the WITS infrastructure is in place, it becomes rather easy to address other issues standing nearby.  For example, in addition to merely knowing the “reason” for the existence of the various files, we may also be interested in questions of file integrity, security, backup, and periodic review.  These issues and more become more tractable once the WITS infrastructure is in place.

##Usage Scenarios for WITS
Jack has many ideas. [All work and no play makes Jack a dull boy.](https://youtube.com/watch?v=4lQ_MjU4QHw)  However, over the years he has accumulated several computers that contain many, many files related to these ideas.  What challenges arise in managing these things and how can WITS help?

###Single Document
Jack has on innumerable occasions drafted various random articles about whatever he's interested in.  For purposes of this example, the idea is “chasing rabbits.”  These documents have been saved on the desktop, or “my documents” of the various computers.  He has repeated the same exercise for the same subject many times.  And on occasion he's found that he cannot save his changes for whatever read-only style woe-of-the-day reason and so has saved the document using a similar name, such as RabbitChasing1.doc.

All of these documents, scattered across the various computers are related.  Jack doesn't want to loose any of them.  In the future, whenever Jack thinks about chasing rabbits, he wants to be able to find all of these documents lest he create even more confusion.   Maybe he could unify them all into one document or even a single directory.  But the problem would only re-emerge in the future.  He's got enough rabbits to chase as it is and doesn't have time for that anyway, so it would be great if he could somehow make a connection between the “idea” of “rabbit chasing” and any number of specific documents, wherever scattered they are.

###A Small Program
Jack has on many occasions downloaded some program from the Internet.  Said program has executable files, documentation, user data, etc.  All of these files live somewhere in Jack's file systems. At some point in the future, Jack may be examining a file system and wonder wtf some of the files are.    It would be great to be able to make a connection between the “idea” of this program and the various files associated with it.

###A Big Program
Jack uses Nginx.  In fact, he has several installations of Nginx in his universe.  The “idea” of Nginx is fairly large and complicated and one of the subjects for Jack's prior described writing has been to organize his notes about Nginx, generally.  Jack has also collected various documents from the Internet talking about the same thing.

In addition to general knowledge about Nginx, it's important to have information about each specific installation of Nginx.  Each installation has executable files, log files, configuration files, maybe even some source code, etc.  In addition, each installation should have the same or similar things. This is starting to look somewhat OO.  For example, Jack might want to define a class **Nginx** and an instance of, for each particular installation.  Each instance should behave the same way and have the same properties.

###A Shared Program
Many programs are shared between several ideas.  For example, an instance of Eclipse has a “workspace” that may contains files for many different projects.  And a single installation of MySQL can support any number of databases, each of which hail from a different project.  These shared spaces can grow cluttered.  It would be nice to link them and their contents back to the original idea.

###A Project
Jack has various large projects.  One project may use Eclipse, XAMPP, and git.  Another project uses Flex Builder, Eclipse, Apache, PHP, and MySQL.  A project like this will yield a blizzard of files in many different locations.  For this project, Jack needs to be able to quickly and easily find specific files (for example, how does he restart the MySQL server on that machine over there?)  And each file must have an answer to the question of “why am I here?”

###Reminders
Certain files or ideas that ought to be reviewed on occasion. 
