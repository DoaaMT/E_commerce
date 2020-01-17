
<img src="Pic/ga.png" alt="GA">


# About the E_commerce website

I created this full stack E-commerce website by using Ruby on Rails and MySQL for both sellers and buyers. 
Users have an ability to put there products to sell and manege it. Also they can view other users products and make an orders.
The user can only edite his own products and orders. 



# The features 
```
 
  def create 
    product = Product.find(params[:order][:product_id])
    @order = Order.new(order_params) 
    @order.user_id = current_user.id
    add_quantity
    @order.save
    redirect_to orders_path
  end
  
    private
    def add_quantity
        product = Product.find(params[:order][:product_id])
        @product = @order.product  
        @product.stock -= @order.quantity
        @product.save
      end

```  
When user add products in his card to make an order, it will be reduce from the stock.
-the technic that i used to swich between players is so simple.. the turn will be 0 for player 1 then it's will be increment to turn 1 for player 2 then decrement again.
- the game had a restart button that will refresh the page for a new game


# List technologies used 
- HTML
- CSS
- JQuery
- Java Script
- Git bash
- GitHub


# Future plan 
- Artificial intelligence (Computer Plays against the player)
- The player can choose the size of game table
- the player can write his name
- the game can count the winner score


# Development process and problem-solving strategy 
- array 
- function
- jquary method
- variable
- img
- for loop
- if condition
- increment
- dicrement  


# wireframes 
<img src="Pic/skra.jpg" alt="wireframes">


# User Stories 
- As a user, I should be able to start a new connect 4 game.
- As a user, I should be able to click on a square to add marker first and then the other marker, and so on.
- As a user, I should be shown a message after each turn for if I win, lose, tie or who's turn it is next.
- As a user, I should not be able to click the same square twice.
- As a user, I should be shown a message when I win, lose or tie.
- As a user, I should not be able to continue playing once I win, lose, or tie
- As a user, I should be able to play the game again without refreshing the page (after finishing the game they can restart the game)


# Pictures for the game

<img src="Pic/Capture0.PNG" alt="Capture 1">
<img src="Pic/Capture1.PNG" alt="Capture 2">
<img src="Pic/Capture2.PNG" alt="Capture 3">
<img src="Pic/Capture3.PNG" alt="Capture 4">
<img src="Pic/Capture4.PNG" alt="Capture 5">
<img src="Pic/Capture5.PNG" alt="Capture 6">


# How i solved the winner 

- I made an empty array for each column.
- for each click the arrays will fills with the player variable .
- for each round will check vertically, horizontally and diagonally.
- if player connect four pieces he wins.



# How my favorite functions work 

```
$('#Restart').click(function() { 
        location.reload();
    });
```    
>  when Restart button are clicked it's will reload the page.


```
   $(".col").click(function(e) { 
```   
> when players clicks any where in the column <div>

 ```
 IDcol = $(this).attr("id"); 
```
> this .attr("id") will return the column id number 
```
IDrow=color(IDcol); 
```
> call the color function that's will colored the circle and return the Row location
```
Check(IDcol,IDrow);      });
```
> call check function, give it coloumn and row id number, check if winner
   
        

# This is the link of the game.. Have fun !
> https://doaamt.github.io/Connect4/index.html





 By Doaa Turkistani 

