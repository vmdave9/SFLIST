# SFLIST
a z/VM tool to view spool files dynamicly

To install SFLIST, first grap the SFLPACK VMARC file from this repository, and upload it to CMS, using binary fixed 80 transfer setting.
Then just unpack it using the CMS VMARC command, and you should then be ready to go.

An overview of SFLIST is                                                           
                                                                              
    The Spool File List Tool (SFList) is intended to make life easier             
    for a class D user when working with spool files. Full-pack RR MDISK          
    overlays for all SPOOL volumes (or OPTION DEVMAINT) are required              
    to view open spool files (e.g. console logs) using the BROWSE request,        
    and support is currently limited to DASD type 3390.                           
                                                                                  
    Command Format                                                                
                                                                                  
    +----------------------------------------------------------------------+       
    |              +---ALL---+                                             |      
    | >>--SFLIST---+---------+------------------------------------------>< |      
    |              +-userid--+                                             |      
    |              +----*----+                                             |      
    +----------------------------------------------------------------------+      
                                                                              
     Parameters                                                                   
                                                                              
      ALL      Indicates that a Spool File Overview  screen should be shown,        
               listing all users on the system that own any spool files,            
               with the corresponding counts for spool files, total records         
               and total spool blocks used. This is also the default.               
               Users are initially listed in descending 'Total Blocks'              
               sequence; an alternate 'ascending userid' sequence can be selec-     
               ted by clicking on the sort dot above the 'File Owner' column.       
                                                                                  
              From this screen you can select spool file details for any of        
              the users simply by placing the cursor on the user-ID and hit-       
              ting ENTER or by double-clicking on the user-ID.                     
                                                                              
      userid   Indicates that a Spool File Details screen should be shown,          
         *     listing all the spool files on the selected user's RDR, PRT          
               and PUN queues (in that sequence). When specifying '*' your          
               own machine's spool files will be listed.                            
               Files within each queue are initially sorted in descending           
               'File Created' date/time sequence, that is, the latest files         
               are on top.                                                          
                Alternate sorting sequences are                                      
              - descending file closed date/time                                   
              - descending file size in spool file blocks                          
              - descending file size in records                                    
              - ascending file name.                                               
              These can be selected by clicking on the sort dots above the         
              headers of the corresponding data columns ('Closed', 'Blocks',       
              'Records' and 'Filename' respectively).                              
                                                                              
     On both of the above screens, and also when using BROWSE, the usual           
     scrolling commands and forward/backward locate are supported.                 

Comments or question to me:
vmdave9@gmail.com
