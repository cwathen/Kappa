# Kappa / timeline of events occuring between two chronological periods and two different sites.

# This can be applied to any timeline and it does not matter how large or small. It's applications are not only for archaeology but can be used to create work schedules etc. 


#use this library to start off

library(vistime)

#using the text of event, etc. will let you edit it to your specific dates. This library requires a month and date so if you are like me and care only about years, then you can use 01-01. 

#Event = Chronological age 
#Group = how you want to group the years together, for instance, by site, by geographical area, etc.
#Start = the start date (YEAR-MONTH-DATE), use 01-01 if month-date are unknown or unspecified
#End = the end date (YEAR-MONTH-DATE), use 01-01 if month-date are unknown or unspecified


data <- read.csv(text="event,group,start,end
 Viking Age,Chronology,0800-01-01,1050-01-01
 Early Medieval Period,Chronology,1050-01-01,1350-01-01
 Wooden Church built,Varnhem,1000-01-01,1000-01-01
 Stone Church built,Varnhem,1030-01-01,1050-01-01
 Fru Sigrid donates estate to Cistercians,Varnhem,1150-01-01,1150-01-01
 Period of cemetery Use,Varnhem,0900-01-01,1150-01-01
 Maximum period of cemetery use,Västerhus,1125-01-01,1500-01-01
 Erection of Frösö runic stone,Västerhus,1050-01-01,1080-01-01
 Pagan burial ceases,Västerhus,1025-01-01,1050-01-01")

#If you want it to aligned with no event labels use this one

gg_vistime(data, optimize_y = TRUE, show_labels = FALSE) 

#If you want the event labels but it won't be aligned

gg_vistime(data, optimize_y = FALSE)
