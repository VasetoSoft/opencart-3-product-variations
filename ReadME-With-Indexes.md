## Update Product Controller - ControllerProductProduct.php
# OpenCart3\catalog\controller\product\product.php

find array of images:

```

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

```
