Installation
============

You have to add require line into you composer.json file. Notice that you need
to override the defined platform name with desired one.

You have to add require line into you composer.json file

.. note:: you need to replace ``platform`` with bundle name you want to
          install

.. code-block:: yaml

    "require": {
       // ...
       "paymentsuite/platform-bundle": "X.X.X"
    }

Then you have to use composer to update your project dependencies

.. code-block:: bash

    $ curl -sS https://getcomposer.org/installer | php
    $ php composer.phar update

And register the bundle in your ``AppKernel.php`` file

.. code-block:: php

    return array(
       // ...
       new PaymentSuite\PaymentCoreBundle\PaymentCoreBundle(),
       new PaymentSuite\PlatformBundle\PlatformBundle(),
    );
