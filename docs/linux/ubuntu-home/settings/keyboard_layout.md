# Keyboard layout

## UA

`/usr/share/X11/xkb/symbols/ua`

```
default partial alphanumeric_keys
xkb_symbols "unicode" {

    include "ua(legacy)"

    name[Group1]= "Ukrainian";

    key <TLDE>  {[      apostrophe,           U02BC,     asciitilde,               U0301 ]};  // ' ʼ ~ ́ (Stress symbol)
    key <AE01>	{[               1,          exclam,       EuroSign                      ]};  // 1 ! €
    key <AE02>	{[               2,        quotedbl,    twosuperior,  doublelowquotemark ]};  // 2 " ² „
    key <AE03>	{[               3,      numbersign,     numerosign, leftdoublequotemark ]};  // 3 # № “
    key <AE04>	{[               4,       semicolon,         dollar,             section ]};  // 4 ; $ §
    key <AE05>	{[               5,         percent,          U20B4                      ]};  // 5 % ₴
    key <AE06>	{[               6,           colon,    asciicircum                      ]};  // 6 : ^
    key <AE07>	{[               7,        question,       sterling                      ]};  // 7 ? £
    key <AE08>	{[               8,        asterisk,         degree,  enfilledcircbullet ]};  // 8 * ° •
    key <AE09>	{[               9,       parenleft,    bracketleft,           braceleft ]};  // 9 ( [ {
    key <AE10>	{[               0,      parenright,   bracketright,          braceright ]};  // 0 ) ] }
    key <AE11>	{[           minus,      underscore,         emdash,              endash ]};  // - _ — –
    key <AE12>	{[           equal,            plus,       notequal,           plusminus ]};  // = + ≠ ±

    key <AD01>	{[ Cyrillic_shorti, Cyrillic_SHORTI,    Cyrillic_je,         Cyrillic_JE ]};                   // й Й ј Ј
    key <AD02>	{[    Cyrillic_tse,    Cyrillic_TSE,  Cyrillic_dzhe,       Cyrillic_DZHE ]};                   // ц Ц џ Џ
    key <AD03>	{[      Cyrillic_u,      Cyrillic_U, Byelorussian_shortu, Byelorussian_SHORTU ]};              // у У ў ў
    key <AD04>	{[     Cyrillic_ka,     Cyrillic_KA,     registered                      ]};                   // к К ®
    key <AD05>	{[     Cyrillic_ie,     Cyrillic_IE,    Cyrillic_io,         Cyrillic_IO ]};                   // е Е ё Ё
    key <AD06>	{[     Cyrillic_en,     Cyrillic_EN,   Cyrillic_nje,        Cyrillic_NJE ]};                   // н Н њ Њ
    key <AD07>  {[    Cyrillic_ghe,    Cyrillic_GHE, Ukrainian_ghe_with_upturn, Ukrainian_GHE_WITH_UPTURN ]};  // г Г ґ Ґ
    key <AD12>	{[    Ukrainian_yi,    Ukrainian_YI, Cyrillic_hardsign,Cyrillic_HARDSIGN ]};                   // ї Ї ъ Ъ

    key <AC02>	{[     Ukrainian_i,     Ukrainian_I,  Cyrillic_yeru,       Cyrillic_YERU ]};  // і І ы Ы
    key <AC08>	{[     Cyrillic_el,     Cyrillic_EL,   Cyrillic_lje,        Cyrillic_LJE ]};  // л Л љ Љ
    key <AC09>	{[     Cyrillic_de,     Cyrillic_DE,    Serbian_dje,         Serbian_DJE ]};  // д Д ђ Ђ
    key <AC11>	{[    Ukrainian_ie,    Ukrainian_IE,     Cyrillic_e,          Cyrillic_E ]};  // є Є э Э

    key <BKSL>	{[       backslash,       bar,      slash,     Ukrainian_ghe_with_upturn ]};  // \ | / ґ

    key <AB02>	{[    Cyrillic_che,    Cyrillic_CHE,   Serbian_tshe,        Serbian_TSHE ]};  // ч Ч ћ Ћ
    key <AB03>	{[     Cyrillic_es,     Cyrillic_ES,      copyright                      ]};  // с С ©
    key <AB06>	{[     Cyrillic_te,     Cyrillic_TE,      trademark                      ]};  // т Т ™
    key <AB08>	{[     Cyrillic_be,     Cyrillic_BE,           less,       guillemotleft ]};  // б Б < «
    key <AB09>	{[     Cyrillic_yu,     Cyrillic_YU,        greater,      guillemotright ]};  // ю Ю > »
    key <AB10>	{[          period,           comma,          slash,            ellipsis ]};  // . , / …

    include "level3(ralt_switch)"
};
```

## US

`/usr/share/X11/xkb/symbols/us`

asciicircum змінив на "Stress symbol"

```
xkb_symbols "basic" {

    name[Group1]= "English (US)";

    key <TLDE>	{[   grave,	 asciitilde	]};
    key <AE01>	{[	 1,	 exclam		]};
    key <AE02>	{[	 2,	 at		]};
    key <AE03>	{[	 3,	 numbersign	]};
    key <AE04>	{[	 4,	 dollar		]};
    key <AE05>	{[	 5,	 percent	]};
    key <AE06>	{[	 6,	 U0301	]};     // asciicircum
    key <AE07>	{[	 7,	 ampersand	]};
    key <AE08>	{[	 8,	 asterisk	]};
    key <AE09>	{[	 9,	 parenleft	]};
    key <AE10>	{[	 0,	 parenright	]};
    key <AE11>	{[   minus,	 underscore	]};
    key <AE12>	{[   equal,	 plus		]};
...
```
