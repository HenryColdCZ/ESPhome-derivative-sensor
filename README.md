# Počítá derivaci za posledních 24 hodin s periodou 1 minuta.
Důležitá funkce je, že hodnoty jsou pamatovány i po výpadku napájení, maximální "ztracené" období je 10 minut což je interval ukládání do flash paměti (viz. flash_write_interval: 10min)
Používám to pro výpočet průměrné spotřeby plynu za posledních 24 hodin v m3/hodinu. Je to vlastně klouzavý průměr spotřeby 
Následně z toho počítám účinnost topení jako poměr z průměrné hodinové spotřeby za posledních 24 hodin a rozdílu mezi vnitřní a venkovní teplotoru.
  - Jednotky účinnosti vyjadřuji jako m³/h/°C tedy kubických metrů plynu za hodinu a stupeň celsia
  - Na vzorku dat za poslední 3 týdny se pohybuji mezi 0,016-0,020m³/h/°C

# Náročnost na hardware
  4x1440byte v RAM paměti (4byte na každý float) 
  4byte ve FLASH paměti 
=> Pro ESP8266 to je v pohodě, i takto je využití RAM jen na 50%

# Vytvořeno ve spolupráci s ChatGPT
