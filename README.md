بسم الله الرحمن الرحيم
In the name of Allah, Most Gracious, Most Merciful

# Quran Image Generator

These are a set of scripts that generate Quran page images based on the old madani fonts provided by the King Fahd Quran Complex in Saudi Arabia. They are currently being used in quran.com and its mobile apps.

The code is copyleft GPL (read: free) but the actual fonts and pages (in the `res/fonts` directory) belong to the [King Fahed Complex in Saudia Arabia](
http://www.qurancomplex.com)


## Installation Summary

```
perl Makefile.PL
make
make install
mysql -u root -p your_password < sql/schema.sql
mysql -u root -p your_password -e "create user 'nextgen'@'localhost' identified by 'nextgen'"
mysql -u root -p your_password -e "grant all privileges on nextgen.* to 'nextgen'@'localhost'"
mysql -u root -p your_password -e "flush privileges"
```

## Usage

`./script/generate.pl --width 1300 --output ./output/ --pages 50`
`./script/generate.pl --width 1300 --output ./output/ --pages 1..3`

## Ayah by ayah images

For ayah by ayah images, see our [legacy branch](https://github.com/quran/quran.com-images/tree/legacy)
