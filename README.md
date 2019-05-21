# phpBB3_fix
fix for when you have the Configurator expected "DOMElement, null given" error

The full error looks like this
```
Fatal error: Uncaught TypeError: Argument 1 passed to s9e\TextFormatter\Configurator\TemplateNormalizations\AbstractNormalization::normalize() m
ust be an instance of DOMElement, null given, 
called in /var/www/html/phpBB3/vendor/s9e/text-formatter/src/Configurator.php on line 7177 and defined in /var/www/html/phpBB3/vendor/s9e/text-formatter/src/Configurator.php:3987 Stack trace: 
#0 /var/www/html/phpBB3/vendor/s9e/text-formatter/src/Configurator.php(7177): s9e\TextFormatter\Configurator\TemplateNormalizations\AbstractNormalization->normalize(NULL) 
#1 /var/www/html/phpBB3/phpbb/textformatter/s9e/factory.php(539): s9e\TextFormatter\Configurator\TemplateNormalizer->normalizeTemplate('<blockquote><xs...') 
#2 /var/www/html/phpBB3/phpbb/textformatter/s9e/factory.php(280): phpbb\textformatter\s9e\factory->get_default_bbcodes(Object(s9e\TextFormatter\Configurator)) 
#3 /var/www/html/phpBB3/phpbb/textformatter/s9e/factory.php(387): phpbb\textformatter\s9e\factory->get_configurator() #4 /var/www/html/phpBB3/phpbb/textformatter/s9e/pa in /var/www/html/phpBB3/vendor/s9e/text-formatter/src/Configurator.php on line 3987
```

Pull down this repo

Extract it to Documents so the files end up in ~/Documents/phpBB3/vendor/...

Open a prompt 
```
cd ~/Documents/phpBB3
chmod +x putFiles.sh
./putFiles.sh
```

Feel free to edit the paths if you put the files somewhere else, or if you're web directory is different

It runs the commands as sudo so it will prompt if necessary

Then go to http://{YOURSITE}/phpBB3 or https for secure sites
