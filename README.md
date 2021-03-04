# VED_CODE4CODEC4SCALE
CONCEPT
mój pomysł na sztuczną metode podnoszenia jakości obrazu lub wideo polegałby na tym że klatka obrazu byłaby przetwarzana z prostych pikseli w układzie plus i widziana jak plaster miodu czyli z plusa na jedną komórkę plastra miodu cz też ośmiooboku równobocznego równoległego - taki jak znak stop a z tych otrzymanych informacji już bedzie znacznie łatwiej skalować 2x czy 4x, można najpierw skalować 2x a pożniej powtórzyć przetwarzanie ale uwaga , tym sposobem doszło by do przekłamań w sąsiadujących plastrach dla tego podczas łaczenia ich w całość musi dojść do uzyskiwania średniej widma koloru i oddania go spowrotem do  wierzchołkowych czyli tych zewnetrznych stykających się pól (które już nie byłyby oryginalnymi bo obraz był wcześniej podwojony) ale to nie logicznie wygląda na przykładzie plusa takżę ta próbka musiałaby byc takim podwójnoramiennym  plusem przed procesem matematycznym dorabiania tych trójkątów powstałych z sumy widma światła widzialnego sąsiednich bloków/pikseli 
I chyba jednak najpierw by było lepiej przeskalować obraz bez algorytmów czyli podwajając wszystko lub razy ileśtam a pożniej dopiero zastosować to wszystko.
podział obrazu na pola plusowe z elementem łączącym i sumaryzacja kolorów w polach, kapnołem się że tak nie dokładnie wygląda plaster miodu ktorego struktore chcialem uzyskac z plusa to wystrczy taki pol ramienny łącznik dorobic ktory ostatecznie tez z dwuch ramion stanie sie jednym
Jak widać na tym najprostszym przykładzie obraz bedzie o   60% powiększony bo 4 trojkąty połowki kwadratu = 2 pola + 2 połówki kwadratu = 1 pole razem 3 a pierwotnie plus skladał sie z 5 pól razem daje 8 pól a to 8 do 5 czyli 16 do 10 = 1,6 razy większy rozmiar obrazu czyli 1920 x 1.6 = 3072 pixeli widh 1728 height
3072x1728 dla przykładu rozdzielczość 3k wynosi 2880x1620.
dodać do tego dobry postprocessing ja bym proponował bazujący na wygładzaniu przy pomocy  współczynnika jasnośći aby otrzymać odpowidnią głebie i ukryć dostrzegalne niedoskonałości. i z obrazu fullhd otrzymuje sie ładny obraz dl ekranu 4K

https://github.com/devegoo/VED_CODE4CODEC4SCALE/blob/main/resample_01.gif
tu są pokazane algorytmy upscalingu dla x2 co daje dwa razy większą powierzchnie ale czy jakość jest przy tym odpowiednia, mój sposób ten który pokazałem jakiś czas temu ma wsþółczynnik x1.6 w jednym przebiegu nie podwajania a jakbym to powidział rozpychania się , jeśli mój algorytm poprzedzi tak akcja jak tu czyli najpierw podwojenie np algorytmem Lanczos IrfanView a następnie rozpychanie lub odwrotnie zależy co lepiej wypadnie w testach wizualnych to współczynnik powiększenia wyniesie ąż x2 x1.6 czyli x3.2 a samym moim algorytmem w dwuch przebiegach 1x1.6x1.6=2.56 
i takie sklaowanie moim algorytmem materiału o rozdzielczości  SD w 2 przebiegach czyli 720x480 na przykład: 720x2.56=1843.2 | 480x2.56=1228.8 (1920 x1080 to FHD). Można powiedzieć że to idealne rozwiązanie a za razem najmniej skomplikowane a przy tym najbardziej dokładne z pośród dotychczas dostępnych aby otrzymać z rozdzielczości większości kanałów SD w DVB-T/S rozdzielczość prawie FullHD bo 1843.2x1228.8 jest też opcja PAL w Europie i Polsce SD 768x576i = po przemianach 1966.08 x 1474.56 .
