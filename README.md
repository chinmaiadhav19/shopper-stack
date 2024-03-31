# shopper-stack
Project Name: shopper stack
Base URL: https://www.shoppersstack.com/shopping
Collection:[shopper profile]
            Request 1:POST register as shopper /shoppers?zoneId=ALPHA
                      Row data : Required,
            Request 2:POST login  users/login
                      Row data : Required,
            Request 3:PATCH Update the shopper Details  /shoppers/{{userId}},
            Request 4:GET Find Shopper data by shopperId  /shoppers/{{userId}},
            Request 5:POST Genarates URL for forgot password  /users/forgot-password
                      Row data : Required,
            Request 6:POST Resets the password  /users/reset-password
                      Row data : Required,
            Request 7:POST Set user password   /users/verify-account?token={{Token}}
                      Row data : Required,
Collection:[Bank Action]
            Request 1:GET Returns all the available bank names  /banks
Collection:[product view action]            
            Request 1:GET Returns all default products  /products/alpha?zoneId=ALPHA
            Request 2:GET Returns all the products   /products?zoneId=ALPHA&token={{Token}}
            Request 3:DELETE Delete an added review  /reviews/{{reviewId}}?productId=5
Collection:[shopper address]  
            Request 1:POST Add a new address  /shoppers/{{userId}}/address
                       Row data : Required,
            Request 2:GET Get all the addresses  /shoppers/{{userId}}/address,
            Request 3:GET Get a particular address by addressId  /shoppers/{{userId}}/address/{{addressId}},
            Request 4:PUT Update an added address   /shoppers/{{userId}}/address/{{addressId}}
                      Row data : Required,
            Request 5:DELETE  Delete an address   /shoppers/{{userId}}/address/{{addressId}}
Collection:[Shopper Bank Account] 
            Request 1:GET Get all bank account of shopper  /bankaccounts?shopperId={{userId}},
            Request 2:POST Create bank account /bankaccounts?bankName=ICD&email={{randomEmail}}&shopperId={{userId}}
                      Row data : Required,
            Request 3:POST Validates bank account credential  /bankaccounts?bankName=ICD
                      Row data : Required,
            Request 4:PATCH Update bank account balance  /bankaccounts?action=CREDITED&amount=40000&number=641852964172        
Collection:[Shopper Bank Cards] 
            Request 1:GET Creates the new card for a given bank   /cards?bankName=ICD&cardType=CREDIT&email={{randomEmail}}&name=chinmai&shopperId={{userId}},
            Request 2:POST Validates bank card with amount   /cards/transaction?amount=3000
                      Row data : Required,
            Request 3:POST Validates bank card  /cards/verify
                      Row data : Required,
            Request 4:PATCH Update card balance  /cards?amount=4000&cardNumber={{cardnumber}}
Collection:[Shopper Cart] 
            Request 1:POST Add a product to the cart  /shoppers/{{userId}}/carts,
            Request 2:GET Get all the products from the cart  /shoppers/{{userId}}/carts,
            Request 3:PUT Update a product in the cart  /shoppers/{{userId}}/carts/121975
                      Row data : Required,
            Request 4:DELETE Delete a product from the cart  /shoppers/{shopperId}/carts/37
Collection:[Shopper Likes Action]        
            Request 1:GET Returns all the likes of shopper  /shoppers/likes?shopperId={{userId}},
            Request 2:PATCH Update the shoppers like list  /shoppers/likes?shopperId={{userId}}
                      Row data : Required,
            Request 3:DELETE delete shoppers like list  /shoppers/likes?shopperId={{userId}}&category=MEN
Collection:[Shopper Order]   
            Request 1:POST Place order from cart  /shoppers/{{userId}}/orders
                      Row data : Required,
            Request 2:GET Display order history  /shoppers/{{userId}}/orders,
            Request 3:GET Generate Invoice copy  /shoppers/{{userId}}/orders/15280/invoice,
            Request 4:PATCH update order status   /shoppers/{{userId}}/orders/{{orderId}}?status=DELIVERED
Collection:[Shopper Product Review related]  
           Request 1:POST Add a review to delivered product  /reviews?productId=5
                      Row data : Required,
            Request 2:GET Get all the reviews of a product  /reviews/productId,
            Request 3:PUT Update an added review  /reviews/{{reviewId}}?productId=5,
            Request 4:DELETE delete an added review  /reviews/{{reviewId}}?productId=5   
Collection:[Shopper Profile Cards]   
            Request 1:POST Save the card data  /cards
                      Row data : Required,
            Request 2:GET get the card data based on type  /cards/{{userId}}?type=DEBIT,
            Request 3:GET Returns all the shoppers cards  /shoppers/cards?cardType=DEBIT&shopperId={{userId}},
            Request 4:DELETE Delete card data based on id  /cards/3256
Collection:[Shopper wishlist]   
            Request 1:POST Add a product to the wishlist  /shoppers/{{userId}}/wishlist
                      Row data : Required,
            Request 2:GET Get all the products from wishlist /shoppers/{{userId}}/wishlist,
            Request 3:DELETE add another product  /shoppers/{{userId}}/wishlist/5
Collection:[Shopper wishlist] 
            Request 2:GET Get all Wallet Transactions  /shoppers/{{userId}}/wallets



            

            
