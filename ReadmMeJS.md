<script type="text/javascript">
    $('.product-options input[type="checkbox"]').bind('click',function() {
        if($(this).prop('checked') === false) {
        $(this).prop('checked', true);
        }
        $('input[type="checkbox"]').not(this).prop("checked", false);
    });
</script>



$('.product-options input[type="checkbox"]').on('change', function() {
    if($(this).prop('checked') === true) {
      console.log(this);
      console.log($(this));
      console.log($(this).prop('selectedIndex'));
      $(this).prop('checked', true);
    }
});






$('.product-options input[type="checkbox]').on('change', function() {
    console.log(idx);
    console.log(elem);
    console.log(this);
    console.log(this.checked);
    console.log($(this));
  });





$('.product-options input[type="checkbox"]').on('change', function() {
    if($(this).prop('checked') === true) {
      console.log(this);
      console.log($(this));
      console.log($(this).prop('selectedIndex'));
      $(this).prop('checked', true);
    }
});




  $('product-options input[type="checkbox]').each(function(idx, elem) {

    console.log(idx);
    console.log(elem);

    $(elem).not(this).prop('checked', false);

    $(elem).on('click', function() {
        if($(this).is(':checked')) {
            $('#product-imgs .slick-track .product-preview.slick-slide').not(".slick-cloned")[idx + 1].click();
        }
    });
});



$('.product-options .checkbox input[type="checkbox"]').change(function () {
      console.log(this);
      console.log($(this));
      console.log($(this).is(':checked'));
      console.log($(this).prop('checked'));
});

$('.product-options .checkbox input[type="checkbox"]').bind('click',function() {

   // console.log($(this).is(':checked'));

      console.log($(this).is(':checked'));
      console.log($(this).prop('checked'));

      if($(this).is(':checked') === true) {
        // alert('haha');
      }

      if($(this).prop('checked') === true) {
        console.log(this);
        console.log($(this));
      }

    if($(this).prop('checked') === true) {
      console.log(this);
      console.log($(this));
    }
    if($(this).prop('checked') === false) {
      $(this).prop('checked', true);
    }
    $('input[type="checkbox"]').not(this).prop("checked", false);
});

$('.product-options .checkbox input[type="checkbox"]').on('change', function() {
    $(this).each(function() {
        if (this.checked) {
          console.log($(this).index());
          console.log($(this).prop('selectedIndex'));
        } else {
            console.log("unchecked");
        }
    });
});

$('.product-options .checkbox input[type="checkbox"]').each(function(i) {
   if (this.checked) {
        console.log(i);
        console.log($(this).index());
        console.log($(this).prop('selectedIndex'));
   }
});