## OpenCart 3 Product Option / Variation - change main image with the product variation image.

# This works with Electronic theme only!

## Update Product Controller - ControllerProductProduct.php
# OpenCart3\catalog\controller\product\product.php

find array of images:

<?php

    // PRODUCT MAIN IMAGES ARRAY

    $data['images'] = array();

    $results = $this->model_catalog_product->getProductImages($this->request->get['product_id']);

    $sliderIndex = 0; // add this

    // in the foreach

    foreach ($results as $result) {

        $sliderIndex++; // add this

        // in data array

        $data['images'][] = array(
            // ...
            // ...
            'sliderIndex' => $sliderIndex, // add this
        );

    }

    // PRODUCT OPTIONS (VARIATIONS) IMAGES ARRAY

    $data['options'] = array();

    foreach ($this->model_catalog_product->getProductOptions($this->request->get['product_id']) as $option) {
        $product_option_value_data = array();

        $optionIndex = 0; // add this

        $product_option_value_data[] = array(
            // ... 
            // ... 
            // ... 
            // ... 
            // ... 
            // ... 
            // ... 
            'optionIndexId'           => $optionIndex, // add this
        );
    }

?>

## Update Product View
# OpenCart3\catalog\view\theme\electronic\template\product\product.twig

<script type="text/javascript">
    $('.radio input:radio').each(function(idx, elem) {
        $(elem).on('click', function() {
            if($(this).is(':checked')) {
                $('#product-imgs .slick-track .product-preview.slick-slide')[idx + 1].click();
            }
        });
    });
</script>