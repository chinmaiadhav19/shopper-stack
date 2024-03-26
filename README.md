# shopper-stack
Project Name: shopper stack
Base URL: https://www.shoppersstack.com/shopping
Collection:[shopper profile]
            Request 1:POST register as shopper /shoppers?zoneId=ALPHA
                      Row data : Required,
            Request 2:POST login  users/login,
            Request 3:PATCH Update the shopper Details  /shoppers/{{userId}},
            Request 4:GET Find Shopper data by shopperId  /shoppers/{{userId}},
            Request 5:POST Genarates URL for forgot password  /users/forgot-password, 
            Request 6:POST Resets the password  /users/reset-password,
            Request 7:POST Set user password   /users/verify-account?token={{Token}}
