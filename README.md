# utl_google_map_of_USA_with_long_and_lat_and_earnings
Create a google map of USA with long and lat and earnings

    ```  Create a google map of USA with long and lat and earnings                                                                                                    ```
    ```                                                                                                                                                               ```
    ```    output                                                                                                                                                     ```
    ```    https://www.dropbox.com/s/fawjrcxk5t9bfck/ggmap_usa.pdf?dl=0                                                                                               ```
    ```                                                                                                                                                               ```
    ```    Google map with bubble size proportional to earnings                                                                                                       ```
    ```                                                                                                                                                               ```
    ```    WORKING CODE                                                                                                                                               ```
    ```       IML/R   WPS/PROC-R                                                                                                                                      ```
    ```                                                                                                                                                               ```
    ```         map <- map<-get_map(location="united states", zoom=3, maptype = "terrain",                                                                            ```
    ```           source="google",color="color");                                                                                                                     ```
    ```         mapPoints <- ggmap(map) +                                                                                                                             ```
    ```           geom_point(aes(y = lat, x = long, size = sqrt(earning)),                                                                                            ```
    ```           data = df, alpha = .5 ,color="darkred") +                                                                                                           ```
    ```           scale_size(range=c(3,20));                                                                                                                          ```
    ```                                                                                                                                                               ```
    ```  see                                                                                                                                                          ```
    ```  https://goo.gl/nQ9dDW                                                                                                                                        ```
    ```  https://stackoverflow.com/questions/45238931/create-a-google-map-of-usa-with-long-and-lat-columns-and-earnings                                               ```
    ```                                                                                                                                                               ```
    ```                                                                                                                                                               ```
    ```  Colin FAY                                                                                                                                                    ```
    ```  https://stackoverflow.com/users/8236642/colin-fay                                                                                                            ```
    ```                                                                                                                                                               ```
    ```                                                                                                                                                               ```
    ```  HAVE                                                                                                                                                         ```
    ```  ====                                                                                                                                                         ```
    ```                                                                                                                                                               ```
    ```  Up to 40 obs SD1.HAVE total obs=4                                                                                                                            ```
    ```                                                                                                                                                               ```
    ```                     capital_                                                                                                                                  ```
    ```  Obs     state      name            lat        long      women    earning                                                                                     ```
    ```                                                                                                                                                               ```
    ```   1     Alabama     Montgomery    32.3615     -86.279     621        832                                                                                      ```
    ```   2     Alaska      Juneau        58.3019    -134.420     797       1008                                                                                      ```
    ```   3     Arizona     Phoenix       33.4485    -112.074     669        827                                                                                      ```
    ```   4     Arkansas    LittleRock    34.7360     -92.331     610        703                                                                                      ```
    ```                                                                                                                                                               ```
    ```  WANT                                                                                                                                                         ```
    ```  ====                                                                                                                                                         ```
    ```                                                                                                                                                               ```
    ```     useful for understanding (different cities plotted)                                                                                                       ```
    ```     Size of bubble is propotional to earnings                                                                                                                 ```
    ```                                                                                                                                                               ```
    ```                                                                                                                                                               ```
    ```     ################################ ##                                                                                                                       ```
    ```     ####     ##   # ___ #    #        #  # ## ####                                                                                                            ```
    ```     ###      ###   / _  \    #        #      ######                       ##                                                                                  ```
    ```     #        # ## | (X) |    #        #      ### #######                 #                                                                                    ```
    ```     ### ######  ###\___ /    ####     #    ##  #########                ##  #                                                                                 ```
    ```              #   ## #         #        ##   ##     ####  #         # ## ##   ##                                                                               ```
    ```     #        #    #############         #    ##    # #   #        ##  ########                                                                                ```
    ```    ##        #       #        ########   #######    ##    #   ####    ## ##                                                                                   ```
    ```    #         #       #        #      ####      ####  #   #           #####                                                                                    ```
    ```    ###################        #         #      ##  ##########      ########                                                                                   ```
    ```    ##  ___#    #################        ########   #        #      ########                                                                                   ```
    ```     # / _  \     #     #        ###########   #    #        ######## #                                                                                        ```
    ```     #| (X) |     #     #        #        ##   ##   #  ####### #######                                                                                         ```
    ```      #\___ /#    #     #        #         #        #### ###  ## ####                                                                                          ```
    ```       #    ##    #     #        #         #      ####    #####   ###                                                                                          ```
    ```       ##     ##  ##################################################                                                                                           ```
    ```        #      ####             #   #      #     ##      ###      ###                                                                                          ```
    ```         #      ##              #   #      #    ########  ######  ###                                                                                          ```
    ```           ##    ##             #   ########    #  #   #  ##   ###                                                                                             ```
    ```            ###  #              #       ## ######  #       ##                                                                                                  ```
    ```              # ##              #           #  ##  #   ##   ##                                                                                                 ```
    ```                  ###############           #  #   #   # ___ #                                                                                                 ```
    ```                            ###             #    # #### / _  \                                                                                                 ```
    ```                              #  ##         #### ######| (X) |                                                                                                 ```
    ```                              ### ##      ##  #####    #\___ /                                                                                                 ```
    ```                                   ##   ##               #  #                                                                                                  ```
    ```                                    ## ##                 #  #                                                                                                 ```
    ```                                     ###                   # #                                                                                                 ```
    ```                                      #                     # #                                                                                                ```
    ```                                                            ###                                                                                                ```
    ```                                                                                                                                                               ```
    ```  *                _              _       _                                                                                                                    ```
    ```   _ __ ___   __ _| | _____    __| | __ _| |_ __ _                                                                                                             ```
    ```  | '_ ` _ \ / _` | |/ / _ \  / _` |/ _` | __/ _` |                                                                                                            ```
    ```  | | | | | | (_| |   <  __/ | (_| | (_| | || (_| |                                                                                                            ```
    ```  |_| |_| |_|\__,_|_|\_\___|  \__,_|\__,_|\__\__,_|                                                                                                            ```
    ```                                                                                                                                                               ```
    ```  ;                                                                                                                                                            ```
    ```                                                                                                                                                               ```
    ```  options validvarname=v7;                                                                                                                                     ```
    ```  libname sd1 "d:/sd1";                                                                                                                                        ```
    ```  data sd1.have;                                                                                                                                               ```
    ```  length state capital_name $12.;                                                                                                                              ```
    ```  input state$ capital_name$ lat long women earning;                                                                                                           ```
    ```  cards4;                                                                                                                                                      ```
    ```  Alabama Montgomery 32.36154 -86.27912 621 832                                                                                                                ```
    ```  Alaska Juneau 58.30194 -134.41974 797 1008                                                                                                                   ```
    ```  Arizona Phoenix 33.44846 -112.07384 669 827                                                                                                                  ```
    ```  Arkansas LittleRock 34.73601 -92.33112 610 703                                                                                                               ```
    ```  ;;;;                                                                                                                                                         ```
    ```  run;quit;                                                                                                                                                    ```
    ```                                                                                                                                                               ```
    ```  *          _       _   _                                                                                                                                     ```
    ```   ___  ___ | |_   _| |_(_) ___  _ __                                                                                                                          ```
    ```  / __|/ _ \| | | | | __| |/ _ \| '_ \                                                                                                                         ```
    ```  \__ \ (_) | | |_| | |_| | (_) | | | |                                                                                                                        ```
    ```  |___/\___/|_|\__,_|\__|_|\___/|_| |_|                                                                                                                        ```
    ```                                                                                                                                                               ```
    ```  ;                                                                                                                                                            ```
    ```                                                                                                                                                               ```
    ```  %utl_submit_r64('                                                                                                                                            ```
    ```   source("c:/Program Files/R/R-3.3.2/etc/Rprofile.site",echo=T);                                                                                              ```
    ```   library(ggmap);                                                                                                                                             ```
    ```   library(haven);                                                                                                                                             ```
    ```   df <- read_sas("d:/sd1/have.sas7bdat");                                                                                                                     ```
    ```   map <- map<-get_map(location="united states", zoom=3, maptype = "terrain",                                                                                  ```
    ```     source="google",color="color");                                                                                                                           ```
    ```   mapPoints <- ggmap(map) +                                                                                                                                   ```
    ```     geom_point(aes(y = lat, x = long, size = sqrt(earning)),                                                                                                  ```
    ```     data = df, alpha = .5 ,color="darkred") +                                                                                                                 ```
    ```     scale_size(range=c(3,20));                                                                                                                                ```
    ```   pdf("d:/pdf/utl_google_map_of_USA_with_long_and_lat_and_earnings.pdf");                                                                                     ```
    ```   mapPoints;                                                                                                                                                  ```
    ```  ');                                                                                                                                                          ```
    ```                                                                                                                                                               ```

