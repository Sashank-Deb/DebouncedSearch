    const search= document.getElementById("search");
    const results= document.getElementById("searchResults");
    //Dummy Data
    const restaurants = [
      { name: 'Italian Pizza', cuisine: 'Italian' },
      { name: 'Thai Curry', cuisine: 'Thai' },
      { name: 'Mexican Tacos', cuisine: 'Mexican' },
      { name: 'Indian Curry', cuisine: 'Indian' },
      { name: 'Japanese Sushi', cuisine: 'Japanese' },
      { name: 'Chinese Noodles', cuisine: 'Chinese' }
    ];

    let timer;
    //Function to search restaurants
    function searchRestaurants(){
      console.count("Search API was fired: ");
      results.innerHTML="";
      let searchedItem= search.value.trim().toLowerCase();
      //Filtering the matching values from the Data
      if (searchedItem.length>1){
        const filteredRestaurants= restaurants.filter((item)=>{
          const filteredName= item.name.trim().toLowerCase().includes(searchedItem);
          const filteredCuisine= item.cuisine.trim().toLowerCase().includes(searchedItem);
          return filteredCuisine || filteredName;
        })
            // Display matching restaurants
            filteredRestaurants.map(restaurant => {
              const li = document.createElement('li');
              li.innerText = restaurant.name + ' - ' + restaurant.cuisine;
              results.appendChild(li);
            });
      }
    }
    //Where all the magic happens
    search.addEventListener('input',()=>{
        clearTimeout(timer);
        timer= setTimeout(searchRestaurants,300);
    })
