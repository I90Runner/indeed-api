Indeed API
===============================================================================

PHP interface to Indeed job search API.

I will write better documentation when I can but look through the source for
more detail.


Example of Usage
-------------------------------------------------------------------------------

    <?php

    require 'indeed-api.php';

    $indeedAPI = new IndeedAPI( 123455667 );
    $indeedAPI->setDefaultParams( array(
        'co' => 'gb'
    ) );

    // Pass a basic query
    $output = $indeedAPI->query('web developer');
    print_r($output);

    // Pass in more options
    $output = $indeedAPI->query(array(
        'q' => 'web developer',
        'l' => 'London',
        'start' => 10,
        'limit' => 3
    ));
    print_r($output);


Author(s)
-------------------------------------------------------------------------------

- Neil Sweeney <neil.sweeney@fubra.com>


Releases
-------------------------------------------------------------------------------

### 1.0.0 (2013-11-21)

Initial release

* Query the job search API
* Pass in default values
* Choose between JSON or XML feed
* Choose to return object or raw document
