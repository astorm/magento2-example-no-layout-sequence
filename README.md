magento2-example-no-layout-sequence
--------------------------------------------------
Example of a module with a sequence set, but whose layout update XML file loads before any other module's.

Try some debugging code here to reproduce

    #File: vendor/magento/framework/View/Model/Layout/Merge.php
    //...
        foreach ($updateFiles as $file) {
            var_dump($file);
            //...
        }    
        
The first file in the list of files will be this module's layout handle XML file.