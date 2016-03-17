# Summary
Python script for syncing data between text files on networked computer.

# Motivation
As part of the IT staff at the Southwest Applied Technology College I encountered an inconvenience for the staff that was beginning to cause problems. We have two label printers in the building that exist on seperate floors that are unable to share saved labels between the two. When someone from one floor went to use the label printer on the other floor they were unable to access anything saved on the other label printer. Both label printers had the ability to export their saved labels but importing labels would overwrite any existing labels, which has happened in the past and had a strong chance of happening again if multiple people tried to import labels. I decided to create this program in order to prevent accidental data loss and to let people save time by using the other label printer when one was in use.

#Instructions for use
To begin the data sync service, start the server program on the computer all other clients will connect to and then start the client program on all other computers with data you want to sync. Provide the source file for syncing on both the server and the client, how long you want to wait between sync attempts on the server, and the IP address of the server on the client as they are started and let them run in the background. Close the client program to stop syncing data with that computer, or close the server to stop all data syncing.

# Important notes
--- The data on a client will not begin being synced when it is initially connected to the server. It needs to wait one cycle before synchronization begins.

--- Clients do not sync together at the exact same time, this is done to prevent lag. Each client syncs with the server when it has waited the stated time to wait on the server.
