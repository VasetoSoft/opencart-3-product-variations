## OpenCart 3 Product Option / Variation - change main image with the product variation image.

# This works with Electronic theme only!

## Update Product View
# OpenCart3\catalog\view\theme\electronic\template\product\product.twig

### This is working for radio buttons, selects and checkboxes product options where the options is predefined and saved.

### SELECT

```
<script type="text/javascript">
    // product-options - select
    $('.product-options select').change(function() {
        console.log($(this).prop('selectedIndex'));
        const idx = $(this).prop('selectedIndex');
        $('#product-imgs .slick-track .product-preview.slick-slide').not(".slick-cloned")[idx].click();
    });
</script>

```

### RADIO BUTTONS

```
<script type="text/javascript">
    $('.product-options .radio input:radio').each(function(idx, elem) {
        console.log(idx);
        $(elem).on('click', function() {
            if($(this).is(':checked')) {
                $('#product-imgs .slick-track .product-preview.slick-slide').not(".slick-cloned")[idx + 1].click();
            }
        });
    });
</script>

```

### CHECKBOXES - single checkbox only

```
<script type="text/javascript">
    
</script>

```

### CHECKBOXES - Multiple checkboxes allowed

```
<script type="text/javascript">
    
</script>

```
