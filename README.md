# utl-Open-GIS-Data-Access-for-the-Commonwealth-of-Pennsylvania
Download PA county shape files and plot Pennsylvania county boundaries 
    StackOverflow: Download PA county shape files and plot Pennsylvania county boundaries                                          
                                                                                                                                   
    Graphic output                                                                                                                 
    https://tinyurl.com/yyctlu9v                                                                                                   
    https://github.com/rogerjdeangelis/utl-Open-GIS-Data-Access-for-the-Commonwealth-of-Pennsylvania/blob/master/pacounty.png      
                                                                                                                                   
    github                                                                                                                         
    https://tinyurl.com/y45nwqpz                                                                                                   
    https://github.com/rogerjdeangelis/utl-Open-GIS-Data-Access-for-the-Commonwealth-of-Pennsylvania                               
                                                                                                                                   
    StackOverflow R                                                                                                                
    https://tinyurl.com/y69ewbsy                                                                                                   
    https://stackoverflow.com/questions/58172017/out-of-bounds-latitude-and-longitude-values-in-converted-shape-file-using-ggplot  
                                                                                                                                   
    Andrew Gustar                                                                                                                  
    https://stackoverflow.com/users/7727429/andrew-gustar                                                                          
                                                                                                                                   
    HOW TO DOWNLAOD THE MAP                                                                                                        
    =======================                                                                                                        
                                                                                                                                   
     To get the county shape file click in download tab on the folloewing page                                                     
                                                                                                                                   
     http://www.pasda.psu.edu/uci/DataSummary.aspx?dataset=24                                                                      
                                                                                                                                   
     PaCounty2019_07.zip  (download this zip)                                                                                      
                                                                                                                                   
     Extract and you will see                                                                                                      
                                                                                                                                   
     PaCounty2019_07.shp                                                                                                           
                                                                                                                                   
    *_                   _                                                                                                         
    (_)_ __  _ __  _   _| |_                                                                                                       
    | | '_ \| '_ \| | | | __|                                                                                                      
    | | | | | |_) | |_| | |_                                                                                                       
    |_|_| |_| .__/ \__,_|\__|                                                                                                      
            |_|                                                                                                                    
    ;                                                                                                                              
                                                                                                                                   
     d:/shp/PaCounty2019_07.shp                                                                                                    
                                                                                                                                   
    *            _               _                                                                                                 
      ___  _   _| |_ _ __  _   _| |_                                                                                               
     / _ \| | | | __| '_ \| | | | __|                                                                                              
    | (_) | |_| | |_| |_) | |_| | |_                                                                                               
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                              
                    |_|                                                                                                            
    ;                                                                                                                              
                                                                                                                                   
    https://tinyurl.com/yyctlu9v                                                                                                   
                                                                                                                                   
    *                                                                                                                              
     _ __  _ __ ___   ___ ___  ___ ___                                                                                             
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|                                                                                            
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                                            
    | .__/|_|  \___/ \___\___||___/___/                                                                                            
    |_|                                                                                                                            
    ;                                                                                                                              
                                                                                                                                   
    * Note it is easy to add layers to this map using lat/log data;                                                                
    * also easy to convert spacial units from census.. gps to lat/lon;                                                             
                                                                                                                                   
    %utl_submit_r64('                                                                                                              
    library(rgdal);                                                                                                                
    library(ggplot2);                                                                                                              
    library(tidyr);                                                                                                                
    library(sp);                                                                                                                   
    dsn <- "d:/shp/PaCounty2019_07.shp";                                                                                           
    map <- readOGR(dsn);                                                                                                           
    map <- spTransform(map, CRS("+proj=longlat +ellps=WGS84 +datum=WGS84"));                                                       
    png("d:/png/pacounty.png",850,500);                                                                                            
    ggplot() +                                                                                                                     
    geom_path(data = map, aes(x = long, y = lat, group = group)) +                                                                 
    labs(title = "ggplot map of pa counties");                                                                                     
    png();                                                                                                                         
    ');                                                                                                                            
