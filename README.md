# cookie
  Set and get Cookie 

# Example:
 
 https://pratik007kumar.github.io/cookie/. 
 
- step1: enter details 
- step2: click on submit
- step3: then reload the page 

# How to use ?
Link js file in your form file  and create copy following function And fill the magic.
```
  function store() {
    //     var exampleFormControlInput1 =$('#exampleFormControlSelect1').val();
    //     setCookie("exampleFormControlSelect1select", exampleFormControlInput1, 30);
    $("form").each(function(){
      var input= $(this).find(':input');
      input.each(function(){
        var value=$(this).val(); 
        var id=$(this).attr('id')
        setCookie(id, value, 30);
        // console.log($(this));
        // console.log(id);
        // console.log(value);
        
      });

    });


  }
  function fetch() {
    // var exampleFormControlInput1=getCookie("exampleFormControlSelect1select");
    // console.log(exampleFormControlInput1);
    

    $("form").each(function(){
      var input= $(this).find(':input');
      input.each(function(){
              // var value=
              var id=$(this).attr('id')
              var value =getCookie(id);
              $(this).val(value); 
              
          // console.log($(this));
          // console.log(id);
          // console.log(value);
          
        });
    });

  }
  function distroy() {
   // var exampleFormControlInput1 =$('#exampleFormControlInput1').val();
   //  setCookie("exampleFormControlInput1", exampleFormControlInput1, -1);
   $("form").each(function(){
    var input= $(this).find(':input');
    input.each(function(){
      var value=$(this).val(); 
      var id=$(this).attr('id')
      setCookie(id, value, -1);
        // console.log($(this));
        // console.log(id);
        // console.log(value);
        
      });
      });
  }

  $( document ).ready(function() {
    console.log( "ready!" );
    var val=getCookie("exampleFormControlInput1");
    if (val != "") {
      if (confirm('Do you want to Use Previous Value')) {
        fetch();
      }else{
        distroy();
      }

    }
  });
  ```
