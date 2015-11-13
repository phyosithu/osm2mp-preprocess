# описание #

Предпроцесс над osm файлом для osm2mp используя osmosis и tag\_transform

# принцип работы #

заменяет комбинацию тегов
> 

&lt;tag k="amenity" v="restaurant"/&gt;


> 

&lt;tag k="cuisine" v="chinese"/&gt;


на
> 

&lt;tag k="mp\_code" v="0x2a04"/&gt;



для osm2mp в poi.cfg добавить для каждого кода

mp\_code 0x2a04 0x2a04

# Пример использования #

для гармина
osmosis --read-xml file=in.osm --tag-transform file=garmin.xml --write-xml file=out.osm

для навитела
osmosis --read-xml file=in.osm --tag-transform file=navitel.xml --write-xml file=out.osm

что сделано
для гармина - типы ресторанов
для навитела дополнительно - места поклонения