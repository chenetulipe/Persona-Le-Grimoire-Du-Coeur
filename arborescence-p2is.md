# L'Arborescence Absolue : Persona 2 Innocent Sin (PSP - ULES01557)

Ce document est la **Bible technique** du projet Persona 2: Innocent Sin FR (PSP). Il couvre l'intégralité du contenu du jeu, de la racine de l'UMD jusqu'aux sous-fichiers enfouis à l'intérieur des archives. Aucun fichier n'est omis, aucun raccourci n'est pris.

Ce document est découpé en **4 parties** :
1. **L'Arborescence Complète** (le Tree)
2. **L'Encyclopédie des Formats** (chaque extension expliquée en profondeur)
3. **Le Lexique de Chaque Fichier** (ce que fait chaque fichier individuellement)
4. **Informations Techniques Avancées** (encodage, opcodes, pipeline de compilation)

---

## PARTIE 1 : L'Arborescence Complète

L'arbre ci-dessous montre la totalité du contenu du disque UMD. Lorsqu'un fichier est un conteneur (comme le CPK ou event.bin), son contenu interne est déroulé en dessous.

```
UMD_ROOT/
├── PERSONA2/
│   ├── UMD_DATA.BIN                                    (48 octets)
│   └── PSP_GAME/
│       ├── ICON0.PNG                                   (14 142 octets)
│       ├── ICON1.PMF                                   (428 032 octets)
│       ├── PARAM.SFO                                   (560 octets)
│       ├── PIC1.PNG                                    (101 499 octets)
│       ├── INSDIR/
│       │   ├── I020EU.DAT                              (258 512 112 octets)
│       │   ├── ICON0.PNG                               (17 748 octets)
│       │   └── PIC1.PNG                                (91 339 octets)
│       ├── SYSDIR/
│       │   ├── BOOT.BIN                                (6 308 604 octets)
│       │   ├── EBOOT.BIN                               (6 308 944 octets)
│       │   ├── OPNSSMP.BIN                             (880 octets)
│       │   └── UPDATE/
│       │       ├── DATA.BIN                            (26 096 016 octets)
│       │       ├── EBOOT.BIN                           (5 540 576 octets)
│       │       └── PARAM.SFO                           (2 080 octets)
│       └── USRDIR/
│           ├── sdata/
│           │   ├── BGMALL.BIN                          (183 977 984 octets)
│           │   └── VOICEALL.BIN                        (9 986 048 octets)
│           ├── pack/
│           │   ├── datapack.bin                        (75 440 octets)
│           │   │   └── [Contient : 2 images GIM]
│           │   ├── movie/
│           │   │   ├── F0141.pmf                       (44 898 304 octets)
│           │   │   ├── F0142.pmf                       (51 646 464 octets)
│           │   │   ├── F0143.pmf                       (12 355 584 octets)
│           │   │   ├── F0144.pmf                       (8 204 288 octets)
│           │   │   ├── F0145.pmf                       (6 977 536 octets)
│           │   │   ├── F0146.pmf                       (6 952 960 octets)
│           │   │   ├── F0147.pmf                       (7 249 920 octets)
│           │   │   ├── F0148.pmf                       (5 052 416 octets)
│           │   │   ├── F0149.pmf                       (5 079 040 octets)
│           │   │   ├── F0150.pmf                       (16 185 344 octets)
│           │   │   ├── F0151.pmf                       (9 545 728 octets)
│           │   │   ├── F0152.pmf                       (22 968 320 octets)
│           │   │   ├── F0153.pmf                       (5 038 080 octets)
│           │   │   ├── F0154.pmf                       (38 924 288 octets)
│           │   │   ├── F0155.pmf                       (9 570 304 octets)
│           │   │   ├── F0156.pmf                       (11 706 368 octets)
│           │   │   ├── F0157.pmf                       (25 479 168 octets)
│           │   │   ├── F0158.pmf                       (10 760 192 octets)
│           │   │   └── F0159.pmf                       (2 516 992 octets)
│           │   └── P2PT_ALL.cpk                        (254 534 848 octets)
│           │       │
│           │       ├── [SCRIPTS ET ÉVÉNEMENTS]
│           │       │   ├── event.bin                   (37 806 080 octets)
│           │       │   │   ├── script_000.bin
│           │       │   │   ├── script_001.bin
│           │       │   │   ├── script_002.bin
│           │       │   │   ├── script_003.bin
│           │       │   │   ├── script_004.bin
│           │       │   │   ├── script_005.bin
│           │       │   │   ├── script_006.bin
│           │       │   │   ├── script_007.bin
│           │       │   │   ├── script_008.bin
│           │       │   │   ├── script_009.bin
│           │       │   │   ├── script_010.bin
│           │       │   │   ├── script_011.bin
│           │       │   │   ├── script_012.bin
│           │       │   │   ├── script_013.bin
│           │       │   │   ├── script_014.bin
│           │       │   │   ├── script_015.bin
│           │       │   │   ├── script_016.bin
│           │       │   │   ├── script_017.bin          (VIDE)
│           │       │   │   ├── script_018.bin
│           │       │   │   ├── script_019.bin
│           │       │   │   ├── script_020.bin
│           │       │   │   ├── script_021.bin
│           │       │   │   ├── script_022.bin
│           │       │   │   ├── script_023.bin
│           │       │   │   ├── script_024.bin
│           │       │   │   ├── script_025.bin
│           │       │   │   ├── script_026.bin
│           │       │   │   ├── script_027.bin
│           │       │   │   ├── script_028.bin
│           │       │   │   ├── script_029.bin
│           │       │   │   ├── script_030.bin
│           │       │   │   ├── script_031.bin
│           │       │   │   ├── script_032.bin
│           │       │   │   ├── script_033.bin
│           │       │   │   ├── script_034.bin
│           │       │   │   ├── script_035.bin          (VIDE)
│           │       │   │   ├── script_036.bin
│           │       │   │   ├── script_037.bin
│           │       │   │   ├── script_038.bin
│           │       │   │   ├── script_039.bin
│           │       │   │   ├── script_040.bin
│           │       │   │   ├── script_041.bin
│           │       │   │   ├── script_042.bin
│           │       │   │   ├── script_043.bin
│           │       │   │   ├── script_044.bin
│           │       │   │   ├── script_045.bin
│           │       │   │   ├── script_046.bin          (VIDE)
│           │       │   │   ├── script_047.bin
│           │       │   │   ├── script_048.bin
│           │       │   │   ├── script_049.bin          (VIDE)
│           │       │   │   ├── script_050.bin          (VIDE)
│           │       │   │   ├── script_051.bin
│           │       │   │   ├── script_052.bin
│           │       │   │   ├── script_053.bin          (VIDE)
│           │       │   │   ├── script_054.bin
│           │       │   │   ├── script_055.bin
│           │       │   │   ├── script_056.bin          (VIDE)
│           │       │   │   ├── script_057.bin
│           │       │   │   ├── script_058.bin
│           │       │   │   ├── script_059.bin
│           │       │   │   ├── script_060.bin
│           │       │   │   ├── script_061.bin
│           │       │   │   ├── script_062.bin
│           │       │   │   ├── script_063.bin          (VIDE)
│           │       │   │   ├── script_064.bin
│           │       │   │   ├── script_065.bin          (VIDE)
│           │       │   │   ├── script_066.bin
│           │       │   │   ├── script_067.bin
│           │       │   │   ├── script_068.bin
│           │       │   │   ├── script_069.bin
│           │       │   │   ├── script_070.bin
│           │       │   │   ├── script_071.bin
│           │       │   │   ├── script_072.bin          (VIDE)
│           │       │   │   ├── script_073.bin          (VIDE)
│           │       │   │   ├── script_074.bin          (VIDE)
│           │       │   │   ├── script_075.bin          (VIDE)
│           │       │   │   ├── script_076.bin          (VIDE)
│           │       │   │   ├── script_077.bin
│           │       │   │   ├── script_078.bin
│           │       │   │   ├── script_079.bin
│           │       │   │   ├── script_080.bin
│           │       │   │   ├── script_081.bin
│           │       │   │   ├── script_082.bin
│           │       │   │   ├── script_083.bin
│           │       │   │   ├── script_084.bin
│           │       │   │   ├── script_085.bin
│           │       │   │   ├── script_086.bin          (VIDE)
│           │       │   │   ├── script_087.bin          (VIDE)
│           │       │   │   ├── script_088.bin          (VIDE)
│           │       │   │   ├── script_089.bin          (VIDE)
│           │       │   │   ├── script_090.bin
│           │       │   │   ├── script_091.bin
│           │       │   │   ├── script_092.bin
│           │       │   │   ├── script_093.bin          (VIDE)
│           │       │   │   ├── script_094.bin          (VIDE)
│           │       │   │   ├── script_095.bin          (VIDE)
│           │       │   │   ├── script_096.bin
│           │       │   │   ├── script_097.bin
│           │       │   │   ├── script_098.bin
│           │       │   │   ├── script_099.bin
│           │       │   │   ├── script_100.bin          (VIDE)
│           │       │   │   ├── script_101.bin
│           │       │   │   ├── script_102.bin
│           │       │   │   ├── script_103.bin          (VIDE)
│           │       │   │   ├── script_104.bin
│           │       │   │   ├── script_105.bin
│           │       │   │   ├── script_106.bin          (VIDE)
│           │       │   │   ├── script_107.bin
│           │       │   │   ├── script_108.bin
│           │       │   │   ├── script_109.bin          (VIDE)
│           │       │   │   ├── script_110.bin
│           │       │   │   ├── script_111.bin
│           │       │   │   ├── script_112.bin
│           │       │   │   ├── script_113.bin
│           │       │   │   ├── script_114.bin
│           │       │   │   ├── script_115.bin
│           │       │   │   ├── script_116.bin
│           │       │   │   ├── script_117.bin
│           │       │   │   ├── script_118.bin          (VIDE)
│           │       │   │   ├── script_119.bin          (VIDE)
│           │       │   │   ├── script_120.bin
│           │       │   │   ├── script_121.bin
│           │       │   │   ├── script_122.bin
│           │       │   │   ├── script_123.bin
│           │       │   │   ├── script_124.bin
│           │       │   │   ├── script_125.bin          (VIDE)
│           │       │   │   ├── script_126.bin          (VIDE)
│           │       │   │   ├── script_127.bin          (VIDE)
│           │       │   │   ├── script_128.bin
│           │       │   │   ├── script_129.bin
│           │       │   │   ├── script_130.bin
│           │       │   │   ├── script_131.bin
│           │       │   │   ├── script_132.bin          (VIDE)
│           │       │   │   ├── script_133.bin
│           │       │   │   ├── script_134.bin
│           │       │   │   ├── script_135.bin          (VIDE)
│           │       │   │   ├── script_136.bin
│           │       │   │   ├── script_137.bin
│           │       │   │   ├── script_138.bin
│           │       │   │   ├── script_139.bin
│           │       │   │   ├── script_140.bin
│           │       │   │   ├── script_141.bin
│           │       │   │   ├── script_142.bin
│           │       │   │   ├── script_143.bin
│           │       │   │   ├── script_144.bin          (VIDE)
│           │       │   │   ├── script_145.bin
│           │       │   │   ├── script_146.bin          (VIDE)
│           │       │   │   ├── script_147.bin
│           │       │   │   ├── script_148.bin          (VIDE)
│           │       │   │   ├── script_149.bin
│           │       │   │   ├── script_150.bin
│           │       │   │   ├── script_151.bin          (VIDE)
│           │       │   │   ├── script_152.bin
│           │       │   │   ├── script_153.bin          (VIDE)
│           │       │   │   ├── script_154.bin
│           │       │   │   ├── script_155.bin          (VIDE)
│           │       │   │   ├── script_156.bin
│           │       │   │   ├── script_157.bin
│           │       │   │   ├── script_158.bin          (VIDE)
│           │       │   │   ├── script_159.bin
│           │       │   │   ├── script_160.bin          (VIDE)
│           │       │   │   ├── script_161.bin
│           │       │   │   ├── script_162.bin          (VIDE)
│           │       │   │   ├── script_163.bin
│           │       │   │   ├── script_164.bin
│           │       │   │   ├── script_165.bin          (VIDE)
│           │       │   │   ├── script_166.bin
│           │       │   │   ├── script_167.bin          (VIDE)
│           │       │   │   ├── script_168.bin
│           │       │   │   ├── script_169.bin          (VIDE)
│           │       │   │   ├── script_170.bin
│           │       │   │   ├── script_171.bin
│           │       │   │   ├── script_172.bin
│           │       │   │   ├── script_173.bin          (VIDE)
│           │       │   │   ├── script_174.bin
│           │       │   │   ├── script_175.bin          (VIDE)
│           │       │   │   ├── script_176.bin
│           │       │   │   ├── script_177.bin
│           │       │   │   ├── script_178.bin
│           │       │   │   ├── script_179.bin          (VIDE)
│           │       │   │   ├── script_180.bin          (VIDE)
│           │       │   │   ├── script_181.bin          (VIDE)
│           │       │   │   ├── script_182.bin          (VIDE)
│           │       │   │   ├── script_183.bin          (VIDE)
│           │       │   │   ├── script_184.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_205.bin
│           │       │   │   ├── script_206.bin          (VIDE)
│           │       │   │   ├── script_207.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_212.bin
│           │       │   │   ├── script_213.bin          (VIDE)
│           │       │   │   ├── script_214.bin
│           │       │   │   ├── script_215.bin          (VIDE)
│           │       │   │   ├── script_216.bin          (VIDE)
│           │       │   │   ├── script_217.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_219.bin
│           │       │   │   ├── script_220.bin          (VIDE)
│           │       │   │   ├── script_221.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_223.bin
│           │       │   │   ├── script_224.bin          (VIDE)
│           │       │   │   ├── script_225.bin
│           │       │   │   ├── script_226.bin
│           │       │   │   ├── script_227.bin          (VIDE)
│           │       │   │   ├── script_228.bin          (VIDE)
│           │       │   │   ├── script_229.bin          (VIDE)
│           │       │   │   ├── script_230.bin          (VIDE)
│           │       │   │   ├── script_231.bin
│           │       │   │   ├── script_232.bin
│           │       │   │   ├── script_233.bin          (VIDE)
│           │       │   │   ├── script_234.bin          (VIDE)
│           │       │   │   ├── script_235.bin          (VIDE)
│           │       │   │   ├── script_236.bin          (VIDE)
│           │       │   │   ├── script_237.bin          (VIDE)
│           │       │   │   ├── script_238.bin          (VIDE)
│           │       │   │   ├── script_239.bin          (VIDE)
│           │       │   │   ├── script_240.bin          (VIDE)
│           │       │   │   ├── script_241.bin          (VIDE)
│           │       │   │   ├── script_242.bin          (VIDE)
│           │       │   │   ├── script_243.bin          (VIDE)
│           │       │   │   ├── script_244.bin          (VIDE)
│           │       │   │   ├── script_245.bin
│           │       │   │   ├── script_246.bin          (VIDE)
│           │       │   │   ├── script_247.bin          (VIDE)
│           │       │   │   ├── script_248.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_283.bin
│           │       │   │   ├── script_284.bin          (VIDE)
│           │       │   │   ├── script_285.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_296.bin
│           │       │   │   ├── script_297.bin          (VIDE)
│           │       │   │   ├── script_298.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_309.bin
│           │       │   │   ├── script_310.bin          (VIDE)
│           │       │   │   ├── script_311.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_321.bin
│           │       │   │   ├── script_322.bin          (VIDE)
│           │       │   │   ├── script_323.bin          (VIDE)
│           │       │   │   ├── script_324.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_327.bin
│           │       │   │   ├── script_328.bin          (VIDE)
│           │       │   │   ├── script_329.bin          (VIDE)
│           │       │   │   ├── script_330.bin          (VIDE)
│           │       │   │   ├── script_331.bin          (VIDE)
│           │       │   │   ├── script_332.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_339.bin
│           │       │   │   ├── script_340.bin          (VIDE)
│           │       │   │   ├── script_341.bin          (VIDE)
│           │       │   │   ├── script_342.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_356.bin
│           │       │   │   ├── script_357.bin          (VIDE)
│           │       │   │   ├── script_358.bin          (VIDE)
│           │       │   │   ├── script_359.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_362.bin
│           │       │   │   ├── script_363.bin          (VIDE)
│           │       │   │   ├── script_364.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_373.bin
│           │       │   │   ├── script_374.bin          (VIDE)
│           │       │   │   ├── script_375.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_383.bin
│           │       │   │   ├── script_384.bin          (VIDE)
│           │       │   │   ├── script_385.bin          (VIDE)
│           │       │   │   ├── script_386.bin          (VIDE)
│           │       │   │   ├── script_387.bin
│           │       │   │   ├── ...
│           │       │   │   ├── script_396.bin
│           │       │   │   ├── script_397.bin          (VIDE)
│           │       │   │   └── script_398.bin          (VIDE)
│           │       │   │   [Total : 399 scripts. 304 avec du contenu, 95 vides]
│           │       │   │
│           │       │   ├── F_BE.BNP                    (2 983 936 octets)
│           │       │   └── TM_EVE.BNP                  (1 396 736 octets)
│           │       │
│           │       ├── [DIALOGUES DE CARTE - MMAP]
│           │       │   ├── MMAP01.BNP                  (499 712 octets)   [Contient 22 images GIM]
│           │       │   ├── MMAP02.BNP                  (464 896 octets)   [Contient 20 images GIM]
│           │       │   ├── MMAP03.BNP                  (350 208 octets)   [Contient 18 images GIM]
│           │       │   ├── MMAP04.BNP                  (313 344 octets)   [Contient 17 images GIM]
│           │       │   ├── MMAP05.BNP                  (143 360 octets)   [Contient 1 image GIM]
│           │       │   └── MMAP06.BNP                  (315 392 octets)   [Contient 14 images GIM]
│           │       │
│           │       ├── [ÉCRAN-TITRE ET MENU PRINCIPAL]
│           │       │   ├── titlecg.bin                 (1 194 928 octets) [Contient 16 images GIM]
│           │       │   └── titlecg2.bin                (38 128 octets)    [Contient 1 image GIM]
│           │       │
│           │       ├── [SYSTÈME, POLICE, MENUS GLOBAUX]
│           │       │   ├── syscg.bin                   (321 712 octets)   [Contient 25 images GIM]
│           │       │   ├── datapack.bin                (75 440 octets)    [Contient 2 images GIM]
│           │       │   ├── messdic_dat.bin             (154 946 octets)
│           │       │   ├── namedic_dat.bin             (22 octets)
│           │       │   ├── branch.bin                  (526 336 octets)
│           │       │   └── bstup.bin                   (2 361 344 octets)
│           │       │
│           │       ├── [INTERFACE DE COMBAT]
│           │       │   ├── bt_menu.bin                 (46 304 octets)    [Contient 10 images GIM]
│           │       │   ├── btef.bin                    (23 856 octets)    [Contient 14 images GIM]
│           │       │   └── cut_in.bin                  (470 720 octets)   [Contient 8 images GIM]
│           │       │
│           │       ├── [MENUS DE COMMANDE]
│           │       │   ├── ch_menu.bin                 (324 672 octets)   [Contient 43 images GIM]
│           │       │   └── cm_menu.bin                 (580 432 octets)   [Contient 33 images GIM]
│           │       │
│           │       ├── [ICÔNES ET PORTRAITS]
│           │       │   ├── advcg.bin                   (3 760 octets)     [Contient 4 images GIM]
│           │       │   ├── gallerycg.bin               (109 488 octets)   [Contient 23 images GIM]
│           │       │   ├── credit.bin                  (537 696 octets)   [Contient 18 images GIM]
│           │       │   ├── entry.bin                   (69 376 octets)    [Contient 3 images GIM]
│           │       │   └── result.bin                  (29 280 octets)    [Contient 8 images GIM]
│           │       │
│           │       ├── [MAGASINS ET BOUTIQUES]
│           │       │   ├── img_bunner.bin              (70 336 octets)    [Contient 26 images GIM]
│           │       │   ├── img_shop.bin                (28 624 octets)    [Contient 9 images GIM]
│           │       │   ├── img_velvet.bin              (124 384 octets)   [Contient 16 images GIM]
│           │       │   └── CD_SHOP.BIN                 (15 312 octets)
│           │       │
│           │       ├── [CASINO - MINI-JEUX]
│           │       │   ├── ca_cmn.bin                  (497 536 octets)   [Contient 16 images GIM]
│           │       │   ├── ca_face.bin                 (113 344 octets)   [Contient 21 images GIM]
│           │       │   ├── ca_hlp.bin                  (68 080 octets)    [Contient 7 images GIM]
│           │       │   ├── card.bin                    (76 688 octets)    [Contient 4 images GIM]
│           │       │   ├── bingo.bin                   (288 624 octets)   [Contient 21 images GIM + 1 CMN Data]
│           │       │   ├── bj.bin                      (202 496 octets)   [Contient 21 images GIM]
│           │       │   ├── poker.bin                   (179 728 octets)   [Contient 6 images GIM]
│           │       │   └── slot.bin                    (196 160 octets)   [Contient 2 images GIM]
│           │       │
│           │       ├── [DONJONS ET CARTE DU MONDE]
│           │       │   ├── LMAP.BNP                    (397 312 octets)   [Contient 3 images GIM]
│           │       │   ├── map_w.bin                   (145 424 octets)   [Contient 47 images GIM]
│           │       │   ├── MCHAR.BNP                   (10 240 octets)    [Contient 3 images GIM]
│           │       │   ├── dunchar.bin                 (137 200 octets)   [Contient 4 images GIM]
│           │       │   ├── edit.bin                    (207 072 octets)   [Contient 21 images GIM]
│           │       │   ├── edit_floor.bin              (536 576 octets)
│           │       │   ├── kiyaku.bin                  (335 760 octets)   [Contient 6 images GIM]
│           │       │   ├── q00.bin                     (65 536 octets)
│           │       │   ├── DNGCOM.BNP                  (112 640 octets)
│           │       │   ├── DNGSCN.BNP                  (137 216 octets)
│           │       │   ├── DUN27.BNP                   (550 912 octets)
│           │       │   ├── DUN28.BNP                   (669 696 octets)
│           │       │   ├── DUN29.BNP                   (380 928 octets)
│           │       │   ├── DUN2A.BNP                   (462 848 octets)
│           │       │   ├── DUN2B.BNP                   (679 936 octets)
│           │       │   └── DUN2C.BNP                   (466 944 octets)
│           │       │
│           │       ├── [MODÈLES 3D - DÉCORS "FIELD"]
│           │       │   ├── F0097.BIN                   (497 664 octets)
│           │       │   ├── F0098.BIN                   (411 648 octets)
│           │       │   ├── F0099.BIN                   (452 608 octets)
│           │       │   ├── F0100.BIN                   (358 400 octets)
│           │       │   ├── F0101.BIN                   (565 248 octets)
│           │       │   ├── F0102.BIN                   (571 392 octets)   [Contient 1 BND Pack]
│           │       │   ├── F0103.BIN                   (387 072 octets)
│           │       │   ├── F0104.BIN                   (432 128 octets)
│           │       │   ├── F0105.BIN                   (262 144 octets)
│           │       │   ├── F0106.BIN                   (462 848 octets)
│           │       │   ├── F0107.BIN                   (466 944 octets)
│           │       │   ├── F0108.BIN                   (450 560 octets)
│           │       │   ├── F0109.BIN                   (456 704 octets)
│           │       │   ├── F0110.BIN                   (419 840 octets)
│           │       │   ├── F0111.BIN                   (450 560 octets)
│           │       │   ├── F0112.BIN                   (444 416 octets)
│           │       │   ├── F0113.BIN                   (466 944 octets)
│           │       │   ├── F0114.BIN                   (485 376 octets)
│           │       │   ├── F0115.BIN                   (483 328 octets)
│           │       │   ├── F0116.BIN                   (428 032 octets)
│           │       │   ├── F0117.BIN                   (299 008 octets)
│           │       │   ├── F0118.BIN                   (442 368 octets)
│           │       │   ├── F0119.BIN                   (491 520 octets)
│           │       │   ├── F0120.BIN                   (438 272 octets)
│           │       │   ├── F0121.BIN                   (258 048 octets)
│           │       │   ├── F0122.BIN                   (452 608 octets)
│           │       │   ├── F0123.BIN                   (448 512 octets)
│           │       │   ├── F0124.BIN                   (438 272 octets)
│           │       │   ├── F0125.BIN                   (438 272 octets)
│           │       │   ├── F0126.BIN                   (450 560 octets)
│           │       │   ├── F0127.BIN                   (442 368 octets)
│           │       │   ├── F0128.BIN                   (299 008 octets)
│           │       │   ├── F0129.BIN                   (466 944 octets)
│           │       │   ├── F0130.BIN                   (485 376 octets)
│           │       │   ├── F0131.BIN                   (483 328 octets)
│           │       │   ├── F0132.BIN                   (428 032 octets)
│           │       │   ├── F0133.BIN                   (442 368 octets)
│           │       │   ├── F0134.BIN                   (442 368 octets)
│           │       │   ├── F0135.BIN                   (448 512 octets)
│           │       │   ├── F0136.BIN                   (319 488 octets)
│           │       │   └── F0849.BIN                   (73 728 octets)
│           │       │
│           │       ├── [EFFETS VISUELS, COMBAT 3D ET DONNÉES DE JEU]
│           │       │   ├── ADDBIN.BIN                  (250 000 octets)   [Contient 4 images GIM]
│           │       │   ├── EFCTALL.BIN                 (1 228 800 octets) [Contient 10 CMN Data]
│           │       │   ├── EVTBG.BNP                   (3 735 552 octets) [Contient 1 BND + 4 CMN]
│           │       │   ├── evttod.bnp                  (911 360 octets)
│           │       │   ├── EVTUNIT.BNP                 (7 884 800 octets)
│           │       │   ├── EVTUNIT2.BNP                (7 507 968 octets)
│           │       │   ├── FBG_EU.BNP                  (124 928 octets)
│           │       │   ├── F_BG_DT.BNP                 (3 764 224 octets) [Contient 3 CMN Data]
│           │       │   ├── F_BG_TM.BNP                 (448 512 octets)
│           │       │   ├── F_MGC_PK.BNP                (23 265 280 octets)[Contient 3 BND + 13 CMN]
│           │       │   ├── MUT_EFFE.BNP                (67 584 octets)
│           │       │   ├── NEW_EBG.BNP                 (7 464 960 octets)
│           │       │   ├── P2P_BPLY.BNP                (217 088 octets)
│           │       │   ├── P2P_DPF.BNP                 (15 046 656 octets)
│           │       │   ├── P2P_DPK.BNP                 (6 338 560 octets)
│           │       │   ├── P_DEMO.BNP                  (34 816 octets)
│           │       │   ├── SMN_EFFE.BNP                (124 928 octets)
│           │       │   └── TM_UNIT.BNP                 (112 640 octets)
│           │       │
│           │       ├── [EFFETS SONORES - SOUND EFFECTS]
│           │       │   ├── SE_BINGO.BIN                (319 136 octets)
│           │       │   ├── SE_BJ.BIN                   (74 608 octets)
│           │       │   ├── SE_BTL.BIN                  (222 240 octets)
│           │       │   ├── SE_DNG.BIN                  (8 519 680 octets)
│           │       │   ├── SE_DVL.BIN                  (69 840 896 octets)[Contient 1 BND Pack]
│           │       │   ├── SE_EVT.BIN                  (8 691 712 octets)
│           │       │   ├── SE_MGC.BIN                  (14 159 872 octets)
│           │       │   ├── SE_PLY.BIN                  (2 889 728 octets) [Contient 1 CMN Data]
│           │       │   ├── SE_POKER.BIN                (205 744 octets)
│           │       │   ├── SE_QUEST.BIN                (120 816 octets)
│           │       │   ├── SE_SLOT.BIN                 (263 792 octets)
│           │       │   ├── SE_STATIC.BIN               (231 280 octets)
│           │       │   ├── SE_SYS.BIN                  (82 112 octets)
│           │       │   ├── SE_TIMEA_00.BIN             (193 904 octets)
│           │       │   ├── SE_TIMEA_01.BIN             (157 344 octets)
│           │       │   ├── SE_VEL1.BIN                 (489 776 octets)
│           │       │   ├── SE_VEL2.BIN                 (293 328 octets)
│           │       │   └── SE_VEL3.BIN                 (42 992 octets)
│           │       │
│           │       ├── [IMAGES GIM INDÉPENDANTES]
│           │       │   ├── m_ef00.gim                  (131 792 octets)
│           │       │   └── m_ef00a.gim                 (131 792 octets)
│           │       │
│           │       └── [IMAGES PNG (POUR PPSSPP)]
│           │           ├── ss_icon0.png                (15 483 octets)
│           │           └── ss_pic1.png                 (122 014 octets)
```

**Statistiques du CPK :**
- Total de fichiers dans le CPK : **136**
- Répartition par extension : 98 `.bin`/`.BIN`, 34 `.bnp`/`.BNP`, 2 `.png`, 2 `.gim`
- Fichier le plus lourd : `SE_DVL.BIN` (~66 Mo)
- Fichier le plus léger : `namedic_dat.bin` (22 octets)

---

## PARTIE 2 : Encyclopédie Complète des Formats de Fichiers

Chaque format rencontré dans le jeu est expliqué ici en profondeur. L'objectif est qu'un romhacker qui ne connaît rien à la PSP puisse comprendre exactement de quoi il s'agit en lisant ces paragraphes.

---

### `.SFO` — System File Object (Sony)

Le fichier `.SFO` est le standard universel de métadonnées de la famille PlayStation (PSP, PS3, PS4, PS Vita). C'est un fichier binaire structuré qui agit comme la **carte d'identité logicielle** du jeu. Lorsque vous insérez un UMD dans la PSP ou que vous chargez une ISO dans PPSSPP, le système lit en tout premier lieu le fichier `PARAM.SFO` pour afficher le nom du jeu, sa région, et vérifier la compatibilité du firmware.

Le format SFO est composé de trois sections binaires : un **Header** (16 octets fixes), une **Table d'Index** (qui mappe les clés aux valeurs), et une **Zone de Données** (qui stocke les chaînes de caractères et les entiers). Les clés les plus importantes sont :
- `DISC_ID` : L'identifiant unique du jeu (pour Persona 2 EU : `ULES01557`)
- `TITLE` : Le nom affiché sur le menu XMB de la PSP
- `PSP_SYSTEM_VER` : La version minimale du firmware requise
- `CATEGORY` : Le type d'application (`UG` = jeu UMD)
- `DISC_VERSION` : La version du jeu (ex: `1.00`)

Ce format est parfaitement documenté et des outils comme `SFO Editor` permettent de le modifier facilement. Dans le contexte du romhacking, on pourrait potentiellement y changer le titre affiché en français, bien que cela ne soit pas prioritaire.

---

### `.PMF` — PlayStation Portable Movie Format (Sony)

Le `.PMF` est le format vidéo propriétaire de Sony, utilisé exclusivement sur la PSP. C'est un conteneur multimédia dérivé du standard MPEG-4 AVC (H.264) pour la vidéo et ATRAC3plus pour l'audio. La PSP possède un **décodeur matériel** dédié (le ME, Media Engine) qui décompresse ces vidéos en temps réel sans solliciter le processeur principal.

Le jeu contient **19 cinématiques** (F0141.pmf à F0159.pmf) totalisant environ 300 Mo. Elles couvrent les moments clés de l'histoire : l'introduction, les invocations de Personas, les scènes dramatiques et la fin du jeu. Ces vidéos sont stockées en dehors du CPK, directement dans `USRDIR/pack/movie/`, car le ME de la PSP a besoin d'un accès séquentiel rapide à ces fichiers pour le streaming.

Fait notable découvert par notre scanner : la cinématique `F0158.pmf` contient étrangement **2 signatures BND Pack** en plus de sa vidéo. Cela pourrait indiquer que cette vidéo embarque des données de sous-titres ou de script d'événement directement dans le flux vidéo.

La résolution native des PMF sur PSP est de **480×272 pixels** à 30 fps. L'audio est en mono ou stéréo à 44.1 kHz. Sur PPSSPP, l'émulateur peut upscaler ces vidéos, mais leur qualité d'origine reste limitée par le codec de l'époque (2011).

---

### `.PNG` — Portable Network Graphics (Standard Web)

Le format PNG est un standard ouvert d'image sans perte de qualité. Dans le contexte de ce jeu PSP, les PNG ne sont utilisés que pour **l'interface du menu XMB de la console** (le menu principal de la PSP, pas du jeu). On en trouve 4 au total :
- `ICON0.PNG` (racine) : L'icône carrée (144×80 px) affichée dans la liste des jeux
- `PIC1.PNG` (racine) : Le fond d'écran panoramique (480×272 px) affiché en arrière-plan
- `INSDIR/ICON0.PNG` : Une version alternative de l'icône pour l'installation de données
- `INSDIR/PIC1.PNG` : Une version alternative du fond d'écran pour l'installation

De plus, dans le CPK, deux fichiers PNG existent :
- `ss_icon0.png` et `ss_pic1.png` : Ce sont des variantes de l'icône et du fond d'écran. Leur présence dans le CPK (plutôt que dans `PSP_GAME/`) est inhabituelle et pourrait servir à un système de sauvegarde ou à une fonctionnalité de partage.

---

### `.CPK` — CRI File System Pack (CRI Middleware)

Le `.CPK` est le format d'archive propriétaire de la société japonaise **CRI Middleware Co., Ltd.**, spécialisée dans les technologies multimédias pour le jeu vidéo. Ce format est extrêmement répandu dans l'industrie du jeu japonais (Atlus, SEGA, Capcom, Bandai Namco, Square Enix...).

Le fichier `P2PT_ALL.cpk` fait **254 Mo** et contient l'écrasante majorité des données du jeu (textes, images, modèles, sons). Structurellement, un CPK est composé de :
1. **Un Header CPK** : Identifie le fichier et sa version
2. **Une TOC (Table Of Contents)** : Un index qui mappe chaque nom de fichier interne à son offset (position en octets) et sa taille dans l'archive
3. **Les Données Compressées** : Les fichiers eux-mêmes, potentiellement compressés avec l'algorithme **CRILAYLA** (une variante propriétaire de LZSS)
4. **Un ITOC (Index Table Of Contents)** : Un index secondaire pour les accès par identifiant numérique

L'extraction est réalisée par l'outil tiers `CriFsLib.GUI.exe` développé par Sewer56. Lors de la recompilation (rebuild) de l'ISO patchée, la TOC doit être **strictement mise à jour** pour refléter les nouvelles tailles des fichiers modifiés, sinon le jeu crashe immédiatement.

---

### `.BNP` — Bind Pack (Atlus)

Le format `.BNP` est un conteneur d'archive propriétaire spécifique au moteur de jeu d'Atlus. Contrairement au CPK qui est un standard de CRI Middleware, le BNP est un format interne d'Atlus utilisé pour **regrouper des données thématiquement liées**.

Un BNP agit comme un "dossier zippé" : il contient plusieurs fichiers de types différents (images, scripts, données binaires) empaquetés séquentiellement. L'analyse par scanner hexadécimal a révélé que :
- Les `MMAP*.BNP` contiennent des **images GIM** (entre 1 et 22) en plus de leurs scripts de dialogue
- Les `DUN*.BNP` contiennent des données de géométrie de donjon
- `F_MGC_PK.BNP` est le plus complexe : il contient 3 sous-archives BND et 13 blocs CMN
- `EVTUNIT.BNP` et `EVTUNIT2.BNP` font chacun ~7.5 Mo et contiennent les modèles 3D des personnages pour les scènes d'événement

La principale difficulté technique avec les BNP est qu'il n'existe **aucune documentation officielle** de leur format. Tout le travail de parsing a été fait par rétro-ingénierie.

---

### `.BIN` (Majuscule) vs `.bin` (Minuscule) — La Grande Différence

C'est l'une des subtilités les plus importantes de ce jeu, et elle est source de confusion permanente.

**`.BIN` en MAJUSCULE** : Ces fichiers sont généralement des **blocs de données brutes et lourds**. Ils se trouvent à la racine de l'UMD (`EBOOT.BIN`, `UMD_DATA.BIN`) ou dans le CPK pour les gros packs monolithiques (`SE_DVL.BIN` qui fait 66 Mo, les `F0*.BIN` qui sont des modèles 3D). Le moteur du jeu les traite comme des flux séquentiels de données brutes sans structure d'archive interne complexe. Bien que le format ISO 9660 (standard de l'UMD) soit en soi insensible à la casse, Atlus a consciemment choisi de nommer ces fichiers en majuscule dans la TOC du CPK pour les différencier.

**`.bin` en minuscule** : Ces fichiers sont des **mini-archives structurées** spécifiques au moteur d'Atlus. Ils contiennent presque toujours des images GIM et/ou des données de jeu organisées avec un header et une table d'offsets. Par exemple, `ch_menu.bin` est un fichier de 324 Ko qui contient à lui seul **43 images GIM** individuelles pour dessiner l'interface du menu de commande. Le moteur d'Atlus les traite comme des "dossiers" en mémoire : il lit le header, parcourt la table d'index, puis charge les assets un par un via leurs offsets.

**Exceptions notables** : `event.bin` (en minuscule) est de loin le plus gros fichier `.bin` du CPK (37 Mo). Bien qu'en minuscule, c'est un cas à part : c'est un immense conteneur compressé CRILAYLA qui renferme les 399 scripts du jeu.

---

### `.GIM` — Graphic Image Map (Sony)

Le `.GIM` (Graphic Image Map) est le format d'image matricielle standard de Sony pour la PSP. Développé par SCE (Sony Computer Entertainment), il est le successeur du `.TIM` (PS1) et du `.TIM2` (PS2) pour la génération PSP.

Contrairement aux formats d'image classiques (PNG, JPEG, BMP), le GIM est conçu pour être **chargé directement dans la mémoire vidéo (VRAM)** de la PSP sans aucun traitement CPU. C'est un format "GPU-ready". Ses caractéristiques techniques :
- **Swizzling** : Les pixels ne sont pas stockés de gauche à droite, de haut en bas comme dans un BMP. Ils sont réarrangés dans un ordre spécial (appelé "swizzle") qui optimise le cache du GPU de la PSP. Cela signifie qu'un GIM ouvert dans un éditeur hexadécimal paraîtra chaotique si on essaie de le lire linéairement.
- **Palettes indexées** : Le GIM supporte les modes 4-bit (16 couleurs), 8-bit (256 couleurs) et 32-bit (true color RGBA). Les modes indexés sont largement utilisés dans ce jeu pour économiser de la VRAM.
- **Canal Alpha** : Le GIM gère nativement la transparence (alpha channel), essentielle pour les éléments d'interface (boutons, boîtes de dialogue avec coins arrondis).
- **Header GIM** : Identifiable par la signature magique `MIG.00.1PSP` (12 octets).

Dans Persona 2 IS, notre scan a détecté un total de **562 images GIM** réparties dans les différentes archives `.bin` et `.BNP`. Elles couvrent absolument toute l'interface du jeu : les portraits des personnages, les boutons des menus, les icônes d'objets, la police d'écriture, les cartes à jouer du casino, etc.

Des outils comme **GimConv** (officiel Sony) ou **GIM2PNG** permettent de convertir ces images en PNG pour les modifier, puis de les reconvertir en GIM.

---

### `.ADX` — ADPCM CRIware (CRI Middleware)

Le `.ADX` est le format audio compressé emblématique du jeu vidéo japonais, développé par CRI Middleware. Il utilise l'encodage **ADPCM** (Adaptive Differential Pulse-Code Modulation), un algorithme de compression audio avec perte qui offre un excellent ratio qualité/taille.

Les caractéristiques clés de l'ADX :
- **Looping natif** : Le format gère nativement les points de boucle (loop points). Une musique ADX peut contenir une intro qui ne joue qu'une fois, puis une section qui boucle à l'infini. C'est crucial pour les musiques de fond (BGM) d'un RPG qui doivent tourner pendant l'exploration ou les combats.
- **Streaming** : L'ADX est conçu pour être streamé (lu en continu) depuis le disque UMD sans charger tout le fichier en mémoire. Cela permet de jouer des musiques longues sans saturer les 32 Mo de RAM de la PSP.
- **Débit** : Typiquement entre 44 et 128 kbps, à 22050 ou 44100 Hz.

Dans Persona 2 IS, l'audio est stocké dans trois grosses banques :
- `BGMALL.BIN` (~175 Mo) : Toute la bande-son du jeu (musiques de fond)
- `VOICEALL.BIN` (~9.5 Mo) : Les doublages vocaux
- Les 18 fichiers `SE_*.BIN` : Les effets sonores, répartis par catégorie (combat, menus, donjons, casino...)

---

### `MSG1` — Atlus Message Script (Atlus)

Le `MSG1` n'est pas une extension de fichier mais une **signature binaire** (Magic Bytes) utilisée par le moteur d'Atlus pour identifier les blocs de texte dans ses jeux. On retrouve ce format dans Persona 2, Persona 3, Persona 4, et les jeux Shin Megami Tensei sur PSP/PS2.

Un bloc MSG1 contient :
- **Les chaînes de caractères** encodées en **Shift-JIS** (l'encodage japonais standard), avec des extensions propriétaires d'Atlus pour les caractères spéciaux
- **Des opcodes de contrôle** (bytecode) intercalés dans le texte. Ces opcodes sont des commandes hexadécimales de 2 octets qui ordonnent au moteur de jeu de réaliser des actions spécifiques (afficher un portrait, jouer un son, attendre l'appui sur un bouton, etc.)
- **Une table de pointeurs** qui indexe chaque entrée de texte par son offset absolu dans le fichier

Pour le projet de traduction française, le parseur (`bin_parser.py`) lit ces blocs MSG1, sépare le texte des opcodes, et génère des fichiers JSON lisibles par un humain. Le traducteur modifie le texte français dans le JSON, puis l'encodeur reconstruit le bloc binaire MSG1 avec les nouveaux textes.

---

### `.GMO` — Graphics Model Object (Sony)

Le `.GMO` est le format standard de modèle 3D sur PSP, développé par SCE. Il est l'équivalent PSP du `.MDL` (Source Engine) ou du `.FBX` (Autodesk). Un fichier GMO encapsule :
- **La géométrie** : Les vertices (sommets) et les faces (triangles) qui composent la forme 3D de l'objet
- **Le squelette d'animation** : La hiérarchie d'os (bones) pour le rigging et l'animation
- **Les matériaux** : Les propriétés de surface (couleur, brillance, transparence) et les références aux textures
- **Les animations** : Les keyframes de mouvement des os

Notre scanner a détecté une signature GMO à l'intérieur de `event.bin`, ce qui signifie que le fichier de scripts principal du jeu contient aussi au moins un modèle 3D. Ce modèle est probablement utilisé pour un objet ou un effet spécial lors d'un événement scriptique.

---

### `BND` — Bind Chunk (Atlus)

Le `BND` n'est pas un fichier indépendant mais une **signature interne** (Magic Bytes) trouvée à l'intérieur d'autres fichiers. C'est un marqueur de sous-archive : lorsque le moteur d'Atlus rencontre cette signature en mémoire, il sait qu'un bloc de données groupées commence.

Notre scanner a trouvé des signatures BND dans : `event.bin` (2), `EVTBG.BNP` (1), `F0102.BIN` (1), `F_MGC_PK.BNP` (3), `SE_DVL.BIN` (1), et même dans `F0158.pmf` (2) et `BGMALL.BIN` (16).

La présence massive de BND dans `BGMALL.BIN` (16 occurrences) est logique : la banque musicale est probablement divisée en 16 sous-sections (par exemple : musiques d'exploration, de combat, de boss, de donjon, de casino, etc.).

---

### `CMN` — Common Data (Atlus)

Le `CMN` est une autre signature interne (Magic Bytes) trouvée dans les fichiers du moteur d'Atlus. Elle marque un **bloc de données partagées** (Common Data) : des variables, des constantes, ou des tables de lookup que plusieurs systèmes du jeu doivent lire simultanément.

Notre scanner a détecté des blocs CMN dans : `EFCTALL.BIN` (10), `F_MGC_PK.BNP` (13), `BGMALL.BIN` (7), `event.bin` (5), `EVTBG.BNP` (4), `F_BG_DT.BNP` (3), `bingo.bin` (1), et `SE_PLY.BIN` (1).

La forte concentration de CMN dans `EFCTALL.BIN` (10 occurrences dans un fichier dédié aux effets) et `F_MGC_PK.BNP` (13 occurrences dans un fichier de 22 Mo lié à la magie) suggère que les données d'effets visuels et de magie sont fortement modulaires et partagées entre les différents systèmes du jeu.

---

### `.DAT` — Data (Générique)

L'extension `.DAT` est l'extension la plus générique qui soit. Elle signifie simplement "données". Dans le contexte de ce jeu, on ne la trouve qu'une seule fois :
- `I020EU.DAT` (258 Mo) dans le dossier `INSDIR/` : C'est le fichier de **Data Install** (installation de données). Lorsque l'utilisateur choisit "Installer les données" sur la PSP physique, ce fichier est copié sur la Memory Stick pour réduire les temps de chargement UMD. Son contenu est essentiellement une copie optimisée de certains fichiers du CPK.

---

## PARTIE 3 : Lexique Détaillé de Chaque Fichier

Voici l'explication individuelle de **chaque fichier** présent dans le jeu. L'objectif est de fournir la même qualité de documentation que les guides de romhacking professionnels (style GameBanana).

---

### Fichiers de la Racine UMD (`PSP_GAME/`)

| Fichier | Taille | Description |
|:---|:---|:---|
| `UMD_DATA.BIN` | 48 octets | Fichier de validation Sony. Contient l'ID du disque `ULES-01557` en texte brut. Sony l'utilise pour vérifier l'authenticité du UMD. |
| `ICON0.PNG` | 14 Ko | Icône du jeu (144×80 px) affichée dans la liste des jeux du menu XMB de la PSP. |
| `ICON1.PMF` | 418 Ko | Animation en boucle de l'icône du jeu. Joue une courte vidéo animée avec du son quand le jeu est sélectionné dans le XMB. |
| `PARAM.SFO` | 560 octets | Carte d'identité du jeu : titre, ID de région, version firmware requise (voir section format SFO). |
| `PIC1.PNG` | 99 Ko | Grand fond d'écran panoramique (480×272) qui s'affiche en arrière-plan du menu XMB quand le jeu est sélectionné. |

### Fichiers d'Installation (`INSDIR/`)

| Fichier | Taille | Description |
|:---|:---|:---|
| `I020EU.DAT` | 246 Mo | Données pré-cachées pour le Data Install sur Memory Stick. Permet de réduire drastiquement les temps de chargement sur PSP physique en évitant la lecture lente du UMD. |
| `ICON0.PNG` | 17 Ko | Version alternative de l'icône pour l'écran d'installation de données. |
| `PIC1.PNG` | 89 Ko | Version alternative du fond d'écran pour l'écran d'installation. |

### Fichiers Système (`SYSDIR/`)

| Fichier | Taille | Description |
|:---|:---|:---|
| `BOOT.BIN` | 6 Mo | Version non chiffrée de l'exécutable principal. Utilisé uniquement par les kits de développement (DevKit) et le mode débogage de la PSP. |
| `EBOOT.BIN` | 6 Mo | **L'exécutable principal du jeu.** C'est le "cerveau" : il contient tout le code compilé du moteur (combat, IA, affichage, physique, audio). Chiffré avec la clé PSP de Sony. |
| `OPNSSMP.BIN` | 880 octets | Module cryptographique MagicGate de Sony. Utilisé pour vérifier et déchiffrer l'EBOOT.BIN au démarrage. |

### Fichiers de Mise à Jour (`SYSDIR/UPDATE/`)

| Fichier | Taille | Description |
|:---|:---|:---|
| `DATA.BIN` | 24 Mo | Données de la mise à jour du firmware PSP incluse sur le disque UMD. |
| `EBOOT.BIN` | 5.2 Mo | Exécutable du programme de mise à jour du firmware. |
| `PARAM.SFO` | 2 Ko | Métadonnées de la mise à jour (version cible du firmware, etc.). |

### Banques Audio (`USRDIR/sdata/`)

| Fichier | Taille | Description |
|:---|:---|:---|
| `BGMALL.BIN` | 175 Mo | **La bande-son complète du jeu.** Contient toutes les musiques de fond (BGM) au format ADX, organisées en 16 sous-sections BND. Inclut les thèmes d'exploration, de combat, de boss, de donjon, du casino, etc. C'est le 2ᵉ plus gros fichier de l'ISO. |
| `VOICEALL.BIN` | 9.5 Mo | **Tous les doublages vocaux.** Contient les lignes parlées des personnages (principalement les invocations de Personas et les exclamations de combat) en format audio compressé. |

### Cinématiques (`USRDIR/pack/movie/`)

| Fichier | Taille | Description |
|:---|:---|:---|
| `F0141.pmf` | 42 Mo | Cinématique d'introduction du jeu (la plus longue FMV). |
| `F0142.pmf` | 49 Mo | Séquence d'ouverture animée (Opening). La plus lourde FMV du jeu. |
| `F0143.pmf` | 11 Mo | Cinématique narrative (événement clé de l'histoire). |
| `F0144.pmf` | 7.8 Mo | Cinématique narrative. |
| `F0145.pmf` | 6.6 Mo | Cinématique narrative. |
| `F0146.pmf` | 6.6 Mo | Cinématique narrative. |
| `F0147.pmf` | 6.9 Mo | Cinématique narrative. |
| `F0148.pmf` | 4.8 Mo | Cinématique narrative. |
| `F0149.pmf` | 4.8 Mo | Cinématique narrative. |
| `F0150.pmf` | 15 Mo | Cinématique narrative longue. |
| `F0151.pmf` | 9.1 Mo | Cinématique narrative. |
| `F0152.pmf` | 21 Mo | Cinématique narrative longue. |
| `F0153.pmf` | 4.8 Mo | Cinématique narrative. |
| `F0154.pmf` | 37 Mo | Cinématique narrative très longue (2ᵉ plus lourde). |
| `F0155.pmf` | 9.1 Mo | Cinématique narrative. |
| `F0156.pmf` | 11 Mo | Cinématique narrative. |
| `F0157.pmf` | 24 Mo | Cinématique narrative longue. |
| `F0158.pmf` | 10 Mo | Cinématique narrative. Contient 2 BND Packs cachés (possible sous-titrage intégré). |
| `F0159.pmf` | 2.4 Mo | Dernière cinématique (la plus courte). Probablement un logo ou un écran de fin. |

---

### Fichiers du CPK — Scripts et Événements

| Fichier | Taille | Contenu Interne | Description |
|:---|:---|:---|:---|
| `event.bin` | 36 Mo | 399 scripts (304 actifs, 95 vides), 1 GMO, 2 BND, 5 CMN | **LE fichier le plus important du jeu.** Contient l'intégralité de la trame narrative, les dialogues de tous les personnages, les événements scriptés (déplacements, combats forcés, changements de carte). Compressé en CRILAYLA. Les scripts vont de `script_000.bin` à `script_398.bin`. |
| `F_BE.BNP` | 2.8 Mo | Données binaires pures | **Les textes de combat (Battle Events).** Contient les lignes de dialogue prononcées pendant les combats, les descriptions des attaques, et les messages système du mode combat. Utilise un Scanner Séquentiel pour la gestion mémoire (l'Algorithme du Delta). |
| `TM_EVE.BNP` | 1.3 Mo | Données binaires pures | **Les sous-titres des cinématiques FMV.** Contient les textes affichés pendant les vidéos PMF. Crucial pour la traduction car ces textes apparaissent en surimpression des cinématiques. |

### Fichiers du CPK — Dialogues de Carte (MMAP)

| Fichier | Taille | Images GIM | Description |
|:---|:---|:---|:---|
| `MMAP01.BNP` | 488 Ko | 22 | **Quartier Hirasaka.** Dialogues des PNJ + portraits/éléments 2D de cette zone. Le quartier le plus riche en PNJ (22 portraits). |
| `MMAP02.BNP` | 454 Ko | 20 | **Quartier Yumezaki.** Dialogues + 20 éléments graphiques. |
| `MMAP03.BNP` | 341 Ko | 18 | **Quartier Aoba.** Dialogues + 18 éléments graphiques. Non traduit. |
| `MMAP04.BNP` | 306 Ko | 17 | **Quartier Kounan.** Dialogues + 17 éléments graphiques. |
| `MMAP05.BNP` | 140 Ko | 1 | **Mont Katatsumuri.** Zone montagneuse avec très peu de PNJ (1 seul portrait). |
| `MMAP06.BNP` | 308 Ko | 14 | **Quartier Rengedai.** Dialogues + 14 éléments graphiques. |

### Fichiers du CPK — Interface du Jeu

| Fichier | Taille | Images GIM | Description |
|:---|:---|:---|:---|
| `titlecg.bin` | 1.1 Mo | 16 | **Écran-titre principal.** Les 16 images composent le logo du jeu, les boutons "Nouvelle Partie", "Continuer", le fond animé, etc. |
| `titlecg2.bin` | 37 Ko | 1 | **Écran-titre secondaire.** Probablement un logo additionnel ou un avertissement. |
| `syscg.bin` | 314 Ko | 25 | **Assets système globaux.** La police d'écriture du jeu, les cadres de boîtes de dialogue, les icônes de sauvegarde, les barres de vie, etc. C'est le fichier UI le plus important. |
| `datapack.bin` | 73 Ko | 2 | **Police de débogage.** Contient une police alternative utilisée par les développeurs pour les messages de debug. |
| `ch_menu.bin` | 317 Ko | 43 | **Menu de commande principal.** Les 43 images GIM dessinent l'intégralité du menu de personnage (statistiques, équipement, Personas, etc.). |
| `cm_menu.bin` | 566 Ko | 33 | **Textures complémentaires du menu.** 33 images additionnelles pour les sous-menus et les onglets. |
| `bt_menu.bin` | 45 Ko | 10 | **Interface de combat.** Les 10 images composent la barre de commande de combat (Attaque, Magie, Défense, Fuite). |
| `btef.bin` | 23 Ko | 14 | **Icônes de combat.** 14 petites icônes (altérations d'état, éléments, types d'attaque). |
| `cut_in.bin` | 459 Ko | 8 | **Portraits "Cut-in".** Les 8 images sont les grands portraits qui apparaissent en plein écran lors des attaques spéciales (invocations de Persona). |
| `advcg.bin` | 3.6 Ko | 4 | **Icônes des joueurs.** 4 petites icônes de personnages. |
| `gallerycg.bin` | 106 Ko | 23 | **Mode Galerie/Film.** 23 images pour l'interface du mode bonus (visionner les cinématiques, écouter la musique). |
| `credit.bin` | 525 Ko | 18 | **Générique de fin.** 18 images composant les crédits (noms des développeurs, logos Atlus/SEGA). |
| `entry.bin` | 67 Ko | 3 | **Saisie du nom.** 3 images pour l'écran de saisie du nom du héros en début de partie. |
| `result.bin` | 28 Ko | 8 | **Écran de résultats.** 8 images affichées après un combat (XP gagnée, objets récupérés, level up). |
| `map_w.bin` | 142 Ko | 47 | **Carte des zones.** 47 images pour l'interface de la carte des différents quartiers de Sumaru City. Le fichier avec le plus d'images GIM du jeu. |

### Fichiers du CPK — Magasins et Boutiques

| Fichier | Taille | Images GIM | Description |
|:---|:---|:---|:---|
| `img_bunner.bin` | 68 Ko | 26 | **Enseignes de magasins.** 26 images pour les bannières et enseignes de chaque boutique de la ville. |
| `img_shop.bin` | 27 Ko | 9 | **Interface des magasins.** 9 images pour le système d'achat/vente (prix, inventaire, boutons). |
| `img_velvet.bin` | 121 Ko | 16 | **Chambre de Velours.** 16 images pour l'interface de fusion de Personas et les services d'Igor. |
| `CD_SHOP.BIN` | 14 Ko | 0 | **Boutique de CDs.** Données et interface de la boutique de musique en jeu. |

### Fichiers du CPK — Casino (Mini-jeux)

| Fichier | Taille | Images GIM | Description |
|:---|:---|:---|:---|
| `ca_cmn.bin` | 486 Ko | 16 | **UI commune du Casino.** 16 images partagées par tous les mini-jeux (table, jetons, fond). |
| `ca_face.bin` | 110 Ko | 21 | **Portraits du Casino.** 21 portraits de personnages qui réagissent pendant les jeux. |
| `ca_hlp.bin` | 66 Ko | 7 | **Aide du Casino.** 7 images pour les écrans d'explication des règles. |
| `card.bin` | 74 Ko | 4 | **Cartes à jouer.** 4 planches de sprites contenant les 52 cartes du jeu + jokers. |
| `bingo.bin` | 282 Ko | 21 (+ 1 CMN) | **Jeu de Bingo.** 21 images pour les grilles et les boules + 1 bloc de données communes. |
| `bj.bin` | 197 Ko | 21 | **Jeu de Blackjack.** 21 images pour la table, les jetons et l'interface. |
| `poker.bin` | 175 Ko | 6 | **Vidéo Poker.** 6 images pour l'interface de la machine à poker. |
| `slot.bin` | 191 Ko | 2 | **Machines à sous.** 2 images (les rouleaux et l'interface). |

### Fichiers du CPK — Donjons et Carte du Monde

| Fichier | Taille | Images GIM | Description |
|:---|:---|:---|:---|
| `LMAP.BNP` | 388 Ko | 3 | **Carte du monde (World Map).** Les 3 images GIM sont la texture de la carte, les icônes de lieux et les labels. |
| `MCHAR.BNP` | 10 Ko | 3 | **Mini-personnages de carte.** 3 sprites des personnages en version chibi (miniature) pour l'affichage sur la carte du monde. |
| `dunchar.bin` | 134 Ko | 4 | **Sprites de donjon.** 4 planches de sprites des personnages jouables vus de dos/face/profil en exploration de donjon. |
| `edit.bin` | 202 Ko | 21 | **Créateur de Donjon.** 21 images pour l'interface du mode création de donjon (un mode bonus). |
| `edit_floor.bin` | 524 Ko | 0 | **Tuiles de sol du Créateur.** Textures de sols pour le mode création. |
| `kiyaku.bin` | 328 Ko | 6 | **Textes du Créateur de Donjon.** 6 images contenant les textes et instructions du mode création. |
| `q00.bin` | 64 Ko | 0 | **Données de quête.** Probable fichier de configuration pour le système de quêtes. |
| `DNGCOM.BNP` | 110 Ko | 0 | **Données communes de donjon.** Paramètres partagés par tous les donjons (taux de rencontre, tables de loot). |
| `DNGSCN.BNP` | 134 Ko | 0 | **Scènes de donjon.** Scripts d'événements spécifiques aux donjons. |
| `DUN27.BNP` | 538 Ko | 0 | **Donjon #27.** Géométrie, textures et données de rencontre d'un donjon spécifique. |
| `DUN28.BNP` | 654 Ko | 0 | **Donjon #28.** |
| `DUN29.BNP` | 372 Ko | 0 | **Donjon #29.** |
| `DUN2A.BNP` | 452 Ko | 0 | **Donjon #2A (hex).** |
| `DUN2B.BNP` | 664 Ko | 0 | **Donjon #2B (hex).** Le plus gros fichier de donjon. |
| `DUN2C.BNP` | 456 Ko | 0 | **Donjon #2C (hex).** |

### Fichiers du CPK — Modèles 3D "Field" (Décors)

Les fichiers `F0*.BIN` contiennent les modèles 3D des environnements explorables de la ville de Sumaru et des lieux importants. Chaque fichier représente un "champ" (field) : un décor 3D complet avec sa géométrie, ses textures, ses données de collision et ses points de spawn.

| Fichier | Taille | Description |
|:---|:---|:---|
| `F0097.BIN` à `F0136.BIN` | 250–570 Ko chacun | **40 décors 3D** de la ville de Sumaru et de ses environs. Chaque fichier est un lieu explorable complet (rue, intérieur de bâtiment, parc, gare, etc.). |
| `F0849.BIN` | 72 Ko | **Décor 3D spécial.** Numéroté bien loin des autres (849 vs 097-136), ce fichier est probablement un environnement de debug ou un lieu secret. |

### Fichiers du CPK — Effets, Modèles et Données de Jeu

| Fichier | Taille | Contenu Interne | Description |
|:---|:---|:---|:---|
| `ADDBIN.BIN` | 244 Ko | 4 images GIM | **Données additionnelles.** Fichier de données supplémentaires avec 4 images (probablement des icônes ou des textures ajoutées après le développement principal). |
| `EFCTALL.BIN` | 1.2 Mo | 10 CMN Data | **Effets visuels globaux.** Tous les effets de particules, de lumière et d'animation du jeu (explosions, éclairs, soins), organisés en 10 blocs de données communes. |
| `EVTBG.BNP` | 3.5 Mo | 1 BND + 4 CMN | **Fonds d'écran des événements.** Les arrière-plans affichés pendant les scènes d'histoire (ciels, paysages, intérieurs). |
| `evttod.bnp` | 890 Ko | 0 | **Time-of-Day des événements.** Données de gestion du cycle jour/nuit pendant les événements scriptés. |
| `EVTUNIT.BNP` | 7.5 Mo | 0 | **Modèles 3D des personnages (Part 1).** Les modèles des personnages tels qu'ils apparaissent pendant les scènes d'histoire (poses, expressions). |
| `EVTUNIT2.BNP` | 7.1 Mo | 0 | **Modèles 3D des personnages (Part 2).** Suite des modèles de personnages. La division en deux fichiers est probablement due à une limite de taille. |
| `FBG_EU.BNP` | 122 Ko | 0 | **Fonds d'écran spécifiques EU.** Variante européenne de certains fonds (probablement des textes légaux ou des logos adaptés). |
| `F_BG_DT.BNP` | 3.5 Mo | 3 CMN | **Données de fond de combat.** Les arrière-plans et données de mise en scène des combats. |
| `F_BG_TM.BNP` | 438 Ko | 0 | **Time Management des fonds de combat.** Gestion temporelle des fonds pendant les séquences de combat. |
| `F_MGC_PK.BNP` | 22 Mo | 3 BND + 13 CMN | **Pack Magie.** Le 2ᵉ plus gros fichier du CPK. Contient tous les effets visuels, animations et données des sorts magiques et des invocations de Personas. 13 blocs CMN = 13 catégories d'effets magiques. |
| `MUT_EFFE.BNP` | 66 Ko | 0 | **Effets de mutation.** Animations d'altérations d'état (poison, confusion, etc.). |
| `NEW_EBG.BNP` | 7.1 Mo | 0 | **Nouveaux fonds de bataille.** Fonds d'écran de combat ajoutés dans la version PSP (absents de la PS1). |
| `P2P_BPLY.BNP` | 212 Ko | 0 | **Données de Battle Play.** Paramètres de gameplay de combat (formules de dégâts, probabilités). |
| `P2P_DPF.BNP` | 14 Mo | 0 | **Data Pack Field.** Pack de données massif pour les environnements de jeu. |
| `P2P_DPK.BNP` | 6 Mo | 0 | **Data Pack (autre).** Pack de données supplémentaire. |
| `P_DEMO.BNP` | 34 Ko | 0 | **Mode Démo.** Données de la démo jouable (séquence automatique si le joueur reste inactif sur l'écran-titre). |
| `SMN_EFFE.BNP` | 122 Ko | 0 | **Effets d'invocation (Summon).** Animations spécifiques aux invocations de Personas. |
| `TM_UNIT.BNP` | 110 Ko | 0 | **Modèles temporels.** Données de timing pour les modèles 3D des unités en combat. |

### Fichiers du CPK — Données Système

| Fichier | Taille | Description |
|:---|:---|:---|
| `messdic_dat.bin` | 151 Ko | **Dictionnaire de messages.** Table de correspondance entre les IDs de messages et les textes du système (menus, descriptions d'objets, noms de sorts). |
| `namedic_dat.bin` | 22 octets | **Dictionnaire de noms.** Extrêmement petit (22 octets), probablement un simple pointeur ou un index vers les noms des personnages principaux. |
| `branch.bin` | 514 Ko | **Données de branchement.** Gère les choix narratifs du joueur et les embranchements de l'histoire (le jeu a quelques moments de choix). |
| `bstup.bin` | 2.2 Mo | **Battle Setup.** Configuration globale des combats : les formations d'ennemis, les tables de rencontre par zone, les paramètres de chaque monstre. |

### Fichiers du CPK — Effets Sonores (SE)

| Fichier | Taille | Description |
|:---|:---|:---|
| `SE_BTL.BIN` | 217 Ko | **Sons de combat.** Bruits d'épées, impacts, tirs, sons de dégâts. |
| `SE_SYS.BIN` | 80 Ko | **Sons système.** Bips de menu, sons de confirmation/annulation, curseur. |
| `SE_DNG.BIN` | 8.1 Mo | **Sons de donjons.** Ambiances sonores des donjons (échos, bruits de pas, portes). |
| `SE_EVT.BIN` | 8.2 Mo | **Sons d'événements.** Effets sonores des scènes scriptées (explosions, cris, portes qui claquent). |
| `SE_DVL.BIN` | 66 Mo | **Sons du Velvet Room / Démon.** Le fichier audio le plus lourd du CPK (66 Mo !). Contient probablement les voix et effets sonores liés aux Personas et à la Chambre de Velours. Contient 1 BND Pack. |
| `SE_MGC.BIN` | 13 Mo | **Sons de magie.** Effets sonores des sorts et des invocations de Personas. |
| `SE_PLY.BIN` | 2.7 Mo | **Sons du joueur.** Bruits de pas, voix de combat des personnages jouables. Contient 1 CMN Data. |
| `SE_BINGO.BIN` | 311 Ko | **Sons du Bingo.** Effets sonores du mini-jeu de Bingo du Casino. |
| `SE_BJ.BIN` | 72 Ko | **Sons du Blackjack.** |
| `SE_POKER.BIN` | 200 Ko | **Sons du Poker.** |
| `SE_SLOT.BIN` | 257 Ko | **Sons des Machines à sous.** |
| `SE_QUEST.BIN` | 118 Ko | **Sons de quête.** Effets sonores liés aux quêtes secondaires. |
| `SE_STATIC.BIN` | 225 Ko | **Sons statiques.** Sons d'ambiance de fond (vent, pluie, foule). |
| `SE_TIMEA_00.BIN` | 189 Ko | **Sons temporels #0.** Effets liés au système de temps/cycle de jeu. |
| `SE_TIMEA_01.BIN` | 153 Ko | **Sons temporels #1.** |
| `SE_VEL1.BIN` | 478 Ko | **Sons Velvet Room #1.** Ambiance et effets de la Chambre de Velours (partie 1). |
| `SE_VEL2.BIN` | 286 Ko | **Sons Velvet Room #2.** (partie 2). |
| `SE_VEL3.BIN` | 42 Ko | **Sons Velvet Room #3.** (partie 3). |

### Fichiers du CPK — Images Indépendantes

| Fichier | Taille | Description |
|:---|:---|:---|
| `m_ef00.gim` | 128 Ko | **Effet visuel de map #0.** Image GIM utilisée comme texture d'effet sur la carte du monde (probablement un effet de lumière ou de particules). |
| `m_ef00a.gim` | 128 Ko | **Effet visuel de map #0 (variante).** Version alternative de l'effet ci-dessus. |
| `ss_icon0.png` | 15 Ko | **Icône de sauvegarde.** Image PNG utilisée pour les screenshots de sauvegarde ou l'icône dans PPSSPP. |
| `ss_pic1.png` | 119 Ko | **Fond de sauvegarde.** Image PNG utilisée comme arrière-plan pour les écrans de sauvegarde. |

---

## PARTIE 4 : Informations Techniques Avancées

Cette section couvre les aspects techniques qui n'ont pas été abordés dans les parties précédentes.

---

### La Compression CRILAYLA (LZSS Propriétaire)

Les fichiers critiques à l'intérieur du CPK (notamment `event.bin`) sont compressés avec l'algorithme **CRILAYLA**, une variante propriétaire du LZSS (Lempel-Ziv-Storer-Szymanski) développée par CRI Middleware.

LZSS fonctionne en remplaçant les séquences de données répétées par des références (offset + longueur) vers des occurrences précédentes. Cela signifie que si le texte "Bonjour Tatsuya" apparaît plusieurs fois dans un script, la première occurrence est stockée en entier, mais les suivantes sont remplacées par un simple pointeur disant "va lire 16 octets à l'offset X".

Le code de décompression se trouve dans `p2is_tool/src/core/compression.py`. Lors de la recompilation du patch, les nouveaux scripts traduits sont recompressés avec cet algorithme avant d'être réinjectés dans le CPK.

---

### L'Algorithme du Delta (F_BE.BNP)

Le fichier `F_BE.BNP` (textes de combat) pose un problème d'ingénierie unique : contrairement à `event.bin` qui utilise une table d'offsets absolus qu'on peut recalculer, F_BE utilise un **Scanner Séquentiel**. Le moteur lit le fichier octet par octet, sans table d'index.

Conséquence : si on ajoute ne serait-ce qu'un seul octet de padding (`0x00`) pour accommoder un texte français plus long que l'original japonais, **tous les offsets suivants sont décalés d'un octet**, ce qui provoque un crash immédiat du type "Invalid Memory Access" (c'est le fameux **Crash Philémon** qui fait sauter directement à la cinématique de Philémon au lieu de jouer la scène normalement).

Pour résoudre ce problème, l'équipe a développé l'**Algorithme du Delta** : au lieu d'ajouter du padding, l'algorithme compacte l'espace binaire de manière purement séquentielle. Si un texte français est plus court que l'original, l'espace gagné est redistribué aux entrées suivantes. Si un texte est plus long, il "emprunte" de l'espace aux entrées voisines plus courtes.

---

### Les Opcodes du Moteur Atlus

Le moteur de jeu d'Atlus utilise un système de **bytecode propriétaire** pour contrôler l'affichage du texte et le déroulement des événements. Ces opcodes sont des commandes hexadécimales de 2 octets (Little Endian) insérées directement dans le flux de texte.

Lors du parsing (décodage), l'outil convertit ces opcodes en **balises textuelles** `[TAG]` pour les protéger pendant la traduction. Le traducteur ne doit jamais supprimer ou déplacer ces balises.

| Opcode (Hex) | Balise | Fonction dans le jeu |
|:---:|:---:|:---|
| `00 22` | `[START]` | Initialise une nouvelle chaîne de caractères en mémoire. Marque le début d'un bloc de texte. |
| `11 07` | `[END]` | Termine la chaîne et réinitialise le buffer d'affichage. Marque la fin d'un bloc de texte. |
| `11 01` | `[NL]` | Retour à la ligne. Force le texte à passer à la ligne suivante dans la boîte de dialogue. |
| `12 08` | `[CHOICE]` | Affiche les options d'un menu contextuel (choix du joueur). |
| `14 31` | `[ANIM]` | Déclenche une animation ou un événement UI (changement de portrait, expression faciale). |
| `02 11` | `[WAIT]` | Instruction de pause. Le jeu attend l'appui sur un bouton avant de continuer. Historiquement responsable de crashs si mal positionnée. |

Autres codes spéciaux :
- `[1113]` : Placeholder pour le **prénom** du héros (saisi par le joueur en début de partie)
- `[1112]` : Placeholder pour le **nom de famille** du héros
- `[SP]` : Espace entre les mots
- `[NULL]` : Marqueur nul (terminaison de chaîne)
- `[E1]`, `[E2]`, `[E3]`, `[E4]` : Délimiteurs de blocs biographiques de personnages

---

### L'Encodage Shift-JIS Atlus et la Table ACCENT_MAP

Le texte du jeu est encodé en **Shift-JIS**, l'encodage standard japonais qui mappe chaque caractère à 2 octets. Cependant, la version européenne du jeu utilise une variante modifiée par Atlus qui supporte les caractères accentués français.

L'outil de traduction (`core/text.py`) contient une table `ACCENT_MAP` qui convertit les caractères accentués français en leurs identifiants de VRAM (Video RAM). Caractères supportés :

> é, è, ê, à, ç, ù, â, î, ô, û, œ, ü, ï, É, È, Ê, À, Ç, Ù, Â, Î, Ô, Û, Œ

Chaque caractère (accentué ou non) coûte **2 octets** dans le budget binaire. La règle de budget est : `Budget = data_size - 8 octets`. Si le texte traduit dépasse ce budget, il faut le raccourcir.

---

### Le Pipeline de Compilation (ISO Rebuild)

La recompilation d'une ISO patchée suit 4 phases strictes :

1. **Extraction** : L'ISO originale est ouverte → `P2PT_ALL.cpk` est isolé → CriFsLib dépaquète le CPK → Les fichiers CRILAYLA (comme `event.bin`) sont décompressés → `event.bin` est découpé séquentiellement en 399 scripts individuels.

2. **Décodage (Parsing)** : Le parseur lit le bytecode Atlus de chaque script binaire → Sépare les opcodes du texte → Génère des fichiers `.json` normalisés avec les champs `nom_orig`, `texte_orig`, `nom_fr`, `texte_fr`.

3. **Encodage (Injection)** : Les fichiers JSON traduits sont validés → Les accents français sont convertis via la table ACCENT_MAP → Les tables de pointeurs absolus sont **intégralement recalculées** → De nouveaux fichiers binaires sont générés.

4. **Rebuild (ISO)** : Les scripts modifiés sont recompressés en CRILAYLA → Réinjectés dans le CPK avec mise à jour stricte de la TOC → L'ISO 9660 est patchée : les secteurs du CPK modifié sont déplacés en fin d'image disque (LBA patching).

---

### Statistiques Globales du Jeu

| Métrique | Valeur |
|:---|:---|
| Taille de l'ISO complète | ~750 Mo |
| Taille du CPK (`P2PT_ALL.cpk`) | 254 Mo |
| Nombre de fichiers dans le CPK | 136 |
| Nombre de scripts d'événement | 399 (304 actifs, 95 vides) |
| Nombre total d'images GIM détectées | 562 |
| Nombre de cinématiques PMF | 19 |
| Nombre de banques sonores SE | 18 |
| Nombre de modèles 3D "Field" | 41 (F0097–F0136 + F0849) |
| Nombre de donjons | 6 (DUN27–DUN2C) |
| Plus gros fichier de l'ISO | BGMALL.BIN (175 Mo) |
| Plus gros fichier du CPK | SE_DVL.BIN (66 Mo) |
| Plus petit fichier du CPK | namedic_dat.bin (22 octets) |
