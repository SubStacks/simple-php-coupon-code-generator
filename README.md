# Simple PHP Coupon Code Generator
[![Latest Stable Version](https://poser.pugx.org/substacks/simple-php-coupon-code-generator/v/stable)](https://packagist.org/packages/substacks/simple-php-coupon-code-generator)
[![Total Downloads](https://poser.pugx.org/substacks/simple-php-coupon-code-generator/downloads)](https://packagist.org/packages/substacks/simple-php-coupon-code-generator)
[![Daily Downloads](https://poser.pugx.org/substacks/simple-php-coupon-code-generator/d/daily)](https://packagist.org/packages/substacks/simple-php-coupon-code-generator)
[![Latest Unstable Version](https://poser.pugx.org/substacks/simple-php-coupon-code-generator/v/unstable)](https://packagist.org/packages/substacks/simple-php-coupon-code-generator)
[![License](https://poser.pugx.org/substacks/simple-php-coupon-code-generator/license)](https://packagist.org/packages/substacks/simple-php-coupon-code-generator)
[![composer.lock](https://poser.pugx.org/substacks/simple-php-coupon-code-generator/composerlock)](https://packagist.org/packages/substacks/simple-php-coupon-code-generator)


Coupon code generator this is php class, which provides the ability to generate coupon codes on various parameters. 
Its key feature is the generation of a coupon code on a mask like this “XXXXXX” or “prefix-XXXX-XXXX-suffix” 
where ‘X’ – random symbol, ‘-’ – custom separator.


### Technology used
HTML, CSS, JS, PHP


### Key Feature
* Support prefix- and –suffix
* Support any coupon mask
  * Support all numbers, alphabets, symbols
  * Support different lenghts
  * Generate N number of coupons
  * Simple Portal
  * Export codes to excel sheet


### Usage
#### SubStacks General Usage
```php
$coupon_code_options = array(</code><br/>
	    'prefix' => '',</code><br/>
	    'suffix' => '',</code><br/>
	    'length' => 10,</code><br/>
	    'letters' => false,</code><br/>
	    'numbers' => true</code><br/>
);
```

```php
$coupon_code = SubStacks\SMS_Marketing\Coupon::generate_coupons($coupon_code_options);
```

1) Dynamic length
```php
	coupon::generate(8);  	// J5BST6NQ
```

2) Using prefix
```php
	coupon::generate(6, ”XYZ-”);    // XYZ-NT163E
```


3) Using suffix
```php
	coupon::generate(6, ”XYZ-”, “-ABC”);    // XYZ-TC2MSD-ABC
```


4) Without numbers
```php
	coupon::generate(6, ””, ””, false);    // LNTDRS
```


5) Without letters
```php
	coupon::generate(6, ””, ””, true, false);    // 835710
```


6) With symbols
```php
	coupon::generate(6, ””, ””, true, true, true);    // #H5&S!7
```


7) Random register (includes lower and uppercase)
```php
	coupon::generate(6, ””, ””, true, true, false, true);    // aT4hB2
```


8) With custom Mask (Note: length does not matter)
```php
	coupon::generate(1, ””, ””, true, true, false, false, “XXXXXX”);    // STG6N8
```


## License
Simple PHP Coupon Code Generator is licensed under the <a href="http://sam.zoy.org/wtfpl/">WTFPL license</a>.
