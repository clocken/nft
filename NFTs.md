# NFTs

- [NFTs](#nfts)
  - [Die praktische Seite](#die-praktische-seite)
    - [Was brauche ich um NFTs zu verkaufen?](#was-brauche-ich-um-nfts-zu-verkaufen)
    - [Welche Kosten entstehen beim Verkauf von NFTs?](#welche-kosten-entstehen-beim-verkauf-von-nfts)
      - [Gas fees ("Benzingebühren")](#gas-fees-benzingebühren)
      - [Zwischenfazit](#zwischenfazit)
    - [Alles weitere](#alles-weitere)
  - [Die technische Seite](#die-technische-seite)
    - [Was ist ein NFT?](#was-ist-ein-nft)
    - [Kann man damit Besitzverhältnisse abbilden?](#kann-man-damit-besitzverhältnisse-abbilden)
    - [Wozu die Blockchain?](#wozu-die-blockchain)
    - [Wozu der Hash?](#wozu-der-hash)

## Die praktische Seite

### Was brauche ich um NFTs zu verkaufen?

Um NFTs zu verkaufen, muss man sie erstellen (wird auch "minting" genannt) und irgendwo anbieten - ein populärer NFT-Marktplatz ist [OpenSea](https://opensea.io/), hier braucht man einen Account. Der Kauf erfolgt normalerweise mit einer Cryptowährung, daher braucht man ein Crypto Wallet, in das die Cryptocoins überwiesen werden können (bei der _Ethereum-Blockchain_ heißen die _Ether bzw. ETH_ bei der Bitcoin-Blockchain _Bitcoin bzw. BTC_) - populär ist [MetaMask](https://metamask.io/) und [Coinbase Wallet](https://www.coinbase.com/wallet). Nach dem Verkauf möchte man sicherlich die Cryptowährung in echtes Geld umwandeln, die Cryptocoins also verkaufen, dafür braucht man einen Account bei einer Cryptobörse - häufig verwendet wird [Coinbase](https://www.coinbase.com/). Zusammengefasst:

- Account bei einem NFT-Marktplatz  --> [OpenSea](https://opensea.io/)
- Ein Crypto Wallet  --> [MetaMask](https://metamask.io/) oder [Coinbase Wallet](https://www.coinbase.com/wallet)
- Account bei einer Cryptobörse  --> [Coinbase](https://www.coinbase.com/)

### Welche Kosten entstehen beim Verkauf von NFTs?

Bei _OpenSea_ werden NFTs in der _Ethereum-Blockchain_ gespeichert (minted) und gehandelt. Durch das Erstellen und Verkaufen von NFTs werden sogenannte Transaktionen in der _Ethereum-Blockchain_ durchgeführt - durch die Transaktionen entstehen die Blöcke in der Blockchain, die durch die sogenannten _Ethereum-Miner_ mit viel Rechenleistung erzeugt werden (bei der Bitcoin-Blockchain sind es die _Bitcoin-Miner_).

#### Gas fees ("Benzingebühren")

Dadurch entstehen Kosten für die Miner, die sogenannten _gas fees_. Diese _gas fees_ werden in _ETH_ (der Cryptowährung _Ether_) bzw. _gwei_ (ein Bruchteil eines _ETH_ - das ist vergleichbar mit € und Cent) bezahlt. Für eine Transaktion wird eine bestimmte Menge an _gas_ (Rechenleistung bzw. technische Ressourcen) vom _Ethereum-Miner_ benötigt und _1 gas_ hat einen bestimmten Preis in _gwei_, den man im [Ethereum Gas Tracker](https://etherscan.io/gastracker) sehen kann - dieser Preis ist [ziemlich schwankend](https://ethereumprice.org/gas/) und man muss sich wohl gut überlegen, wann man eine Transaktion durchführen lassen möchte, zumal ich bisher nirgends rausfinden konnte, wie viel _gas_ die Transaktionen beim NFT-Erstellen bzw. NFT-Verkauf durchschnittlich benötigen und daher nicht ausrechnen konnte, wie viel _gwei_ oder _ETH_ sie nun wirklich kosten, was aber bei den schwankenden Preisen ohnehin nur eine Momentaufnahme wäre. Um _gas fees_ zu vermeiden, kann man wohl die sogenannte [_Polygon-Blockchain_ verwenden](https://support.opensea.io/hc/en-us/articles/4404029357587) - da habe ich mich nicht mit beschäftigt, es entstehen aber wohl Kosten beim sogenannten ["Bridging" von Polygon zu Ethereum](https://support.opensea.io/hc/en-us/articles/4401888867091).

Bei _OpenSea_ werden _Gebote_ auf NFTs (also bei Auktionen) nicht direkt in [_ETH_ bezahlt, sondern in _WETH_ (Wrapped ETH)](https://support.opensea.io/hc/en-us/articles/1500003246082). Das _WETH_ muss man in _ETH_ umwandeln, damit man es sich an einer Cryptobörse als echtes Geld auszahlen lassen kann, durch das Umwandeln entsteht wiederum eine Transaktion, die eine _gas fee_ kostet. Bei NFT-Verkäufen zum Festpreis wird wohl direkt in _ETH_ gezahlt.

Neben den _gas fees_ für die Transaktionen beim Erstellen und Verkaufen von NFTs nimmt [OpenSea beim Verkauf eine _service fee_ von 2,5% des Verkaufspreises](https://support.opensea.io/hc/en-us/articles/360063498333). Das Auszahlen von _ETH_ in echtem Geld an einer Cryptobörse kostet ebenfalls eine [gewisse Gebühr](https://help.coinbase.com/en/coinbase/trading-and-funding/pricing-and-fees/fees). Zusätzlich könnte es sein, dass [Steuern auf NFT-Verkaufserlöse](https://www.haufe.de/taxulting/non-fungible-token-nft-richtig-versteuern_484580_544638.html) fällig werden.

Natürlich muss jeder Auftrag für eine Transaktion über das Wallet bestätigt werden (aus dem Wallet wird ja das _ETH_ bzw. _gwei_ dann abgebucht) und man sieht, wie viel die Transaktion ca. kosten wird, aber ich weiß z. B. nicht, ob es beim Verkauf eines NFTs eine bestimmte Frist gibt, bis wann die Transaktion durchgeführt sein muss oder ob das einfach automatisch läuft und das dann automatisch vom Wallet abgebucht wird.

_Gas fees_ werden immer in _ETH_ bzw. _gwei_ gezahlt, was bedeutet, dass man immer einen gewissen Bestand an _ETH_ in seinem Wallet haben muss, mit dem die _gas fees_ beglichen werden können (den Bestand muss man ggf. bei einer Cryptobörse vorher kaufen).

Neben den ganzen Abzügen vom Gewinn gibt es aber auch ein positives "Feature" bei _OpenSea_: die [Creator earnings](https://support.opensea.io/hc/en-us/articles/1500009575482). Das sind Gebühren von bis zu 10% (kann der NFT-Ersteller selbst festlegen), die beim Weiterverkaufen von NFTs entstehen und an den Ersteller des NFTs gezahlt werden. Kann man wohl in etwa mit [GEMA-Gebühren](https://www.gema.de/die-gema/das-wichtigste-zu-den-gema-gebuehren/) vergleichen, die nicht bei Kunstwerknutzung sondern Kunstwerkverkauf gezahlt werden müssen.

#### Zwischenfazit

Insgesamt ist es meiner Ansicht nach relativ undurchsichtig welche Kosten beim Verkauf von NFTs entstehen. Nirgends konnte ich eine klare Aufstellung finden, wann und wie viele Transaktionen bei verschiedenen Aktionen auf dem OpenSea-Marktplatz entstehen. Hinzu kommen die stark schwankenden Kurse der Cryptowährung _ETH_, die es nach meiner Ansicht nahezu unmöglich machen genaue €-Preise für den Verkauf und den tatsächlichen Gewinn im Vorfeld anzugeben. Was man sich heute vielleicht irgendwie mühsam zusammenrechnet muss morgen nicht und auf keinen Fall nächste Woche genau so sein. Ferner sind die Kosten sicherlich auch von NFT-Marktplatz zu NFT-Marktplatz unterschiedlich.

Ich versuche hier trotzdem mal die [Kostenübersicht bei OpenSea](https://support.opensea.io/hc/en-us/articles/1500006315941) zusammenzufassen. Wie gesagt, konnte ich nicht im Detail herausfinden welche Transaktionen wirklich nötig werden, sondern habe immer nur gesehen, wann man _gas fees_ bezahlen muss.

Einmalige _gas fees_ für:

- [zwei Transaktionen bei Account Erstellung bzw. Aktivierung für NFT-Handel](https://support.opensea.io/hc/en-us/articles/1500003246262)

Wiederkehrende _gas fees_ für:

- Annahme von Geboten bei NFT-Auktionen
- Übertragen oder Verschenken von NFTs (ob der Verkauf zu einem Festpreisangebot als "Übertragen" gilt, weiß ich nicht)
- Abbrechen eines Verkaufsangebots von NFTs, [+1 für jedes vorherige Senken eines Festpreisangebotes](https://support.opensea.io/hc/en-us/articles/4410153816723)
- _WETH_ in _ETH_ umwandeln (und umgekehrt)

### Alles weitere

Ich empfehle, sich ein wenig durch das [Help Center von OpenSea](https://support.opensea.io/hc/en-us) zu lesen. Das ist manchmal etwas mühselig, weil es in so einem Frage-Antwort-Schema aufgebaut ist und man manchmal suchen muss, bis man eine halbwegs befriedigende Antwort zu dem findet, was man wissen möchte. Dennoch ist es meiner Meinung nach wichtig, um Kostenüberraschungen zu vermeiden; man sollte möglichst genau verstehen, wie viel Verkaufserlös am Ende wirklich rauskommt.

Abschließend noch zwei Videos zu NFTs:

- [Einfache Video-Erklärung](https://yewtu.be/watch?v=uVTMALeu_I4), was NFTs sind und ob es sich lohnt seine Kunst als NFT zu verkaufen oder lieber woanders. Die ist etwas nervig, aber was sie erzählt, scheint mir sinnvoll zu sein - wenn auch technisch teils nicht ganz korrekt
- [Video mit Tips](https://yewtu.be/watch?v=mj-OgSlX2UE), wie man NFT-Angebote setzen sollte, um _gas fees_ klein zu halten

---

## Die technische Seite

### Was ist ein NFT?

NFT steht für Non Fungible Token - zu deutsch: Nicht austauschbarer Token.

Ein Token ist technisch gesehen erstmal nur ein identifizierbares Merkmal oder ein Platzhalter für etwas. Z. B. heißen Spielsteine, wie Poker-Chips, auf englisch auch Token. Beim Poker sind sie eben ein Platzhalter für echtes Geld, bspw. _blauer Chip = 50 Cent_. Allerdings sind Poker-Chips _austauschbar_ - ein blauer Chip kann gegen einen beliebigen anderen blauen Chip ausgetauscht werden, ohne seine Bedeutung zu verlieren. Jeder blaue Chip steht immer für 50 Cent in unserem Beispiel. Und 50 Cent sind immer 50 Cent.

Was sind nun Beispiele für nicht austauschbare Token? Ein Haustürschlüssel ist z. B. ein nicht austauschbarer Token. Er passt ausschließlich in eine Haustür (von Generalschlüsseln mal abgesehen ;)) und ein anderer Schlüssel kann nicht an seiner Stelle verwendet werden - man kann ihn also nicht gegen einen beliebigen anderen Schlüssel austauschen ohne dass seine Bedeutung verloren geht. Man kann auch sagen, dass mit dem Haustürschlüssel die Haustür (bzw. das Schloss) identifiziert werden kann. Hätte man drei Schlüssel-Schloss-Kombinationen und sie mit 1, 2, 3 beschriftet wüsste man direkt, dass Schlüssel 1 nur zu Schloss 1 gehören kann und hätte das Schloss eindeutig identifiziert.

Die obigen Beispiele kommen aus der echten Welt. Indentifizierende Tokens gibt es aber auch in der virtuellen Welt. Ein Beispiel sind sogenannte _Hashes_. Das sind Zeichenketten, die aus Dateien (genauer aus Bitströmen, also einer Folge aus 1en und 0en) generiert werden können und immer eindeutig sind. Man kann mit einem Hash also eine Datei identifizieren. Bspw. ist der Hash des folgenden Bildes "_5b55704f60c550fc594c65d5e3032b10eee43eeb_"

![Cryptopunks.jpg](./Cryptopunks.jpg)

Würde auch nur ein Pixel des Bildes verändert, dann würde sich auch der Hash ändern, den man daraus generiert.

### Kann man damit Besitzverhältnisse abbilden?

Weil von Dateien immer beliebig viele Kopien erzeugt werden können, ist es schwierig in der virtuellen Welt einen eindeutigen Besitzer einer Datei festzulegen. Man kann den Urheber versuchen zu benennen, aber nicht mal das ist immer einfach.

Wie in der echten Welt normalerweise der Besitzer des Haustürschlüssels auch der Besitzer der Haustür (bzw. des Hauses) ist (Mieter berücksichtigen wir hier mal nicht ;)), könnte man nun sagen: Wer den Hash einer Datei besitzt, besitzt auch die Datei aus der er generiert wurde. Hätte jemand den obigen Hash "_5b55704f60c550fc594c65d5e3032b10eee43eeb_" in einer Textdatei auf seinem Computer gespeichert, könnte er den Hash auf Anfrage vorzeigen und damit sagen: Ich _besitze_ das obige Bild.

Nun muss man aber bedenken, dass Dateien ja beliebig kopiert werden können. Also könnte jemand anderes eine Kopie der Textdatei machen und selbst den Hash vorzeigen und behaupten, er wiederum sei Besitzer des obigen Bildes - niemand könnte nun eindeutig sagen, wer der "echte" Besitzer der Datei ist. (Man braucht nicht mal Zugriff auf die Textdatei haben, weil es sehr leicht ist den Hash zu einer Datei zu generieren.) Allein der Besitz des Hashes reicht also nicht aus, um einen Besitzer eindeutig zu kennzeichnen. Hier kommt nun die _Blockchain_ ins Spiel.

Das vorige Beispiel mit dem Haustürschlüssel war genau genommen etwas verkürzt dargestellt. Eigentlich ist es ja nicht der Besitz des Haustürschlüssels der den Besitz des Hauses kennzeichnet, sondern der Kaufvertrag. Ein Schlüsseldieb kann ja nicht zweifelsfrei behaupten, dass er das Haus besitzt, zu dem er den Schlüssel gestohlen hat. Der "Dieb" des Hashes einer Datei könnte das allerdings behaupten, wie oben gesehen. Die _Blockchain_ ermöglicht es nun einen Kaufvertrag (mit einer Cryptowährung) für den Hash abzuschließen und sicher abzuspeichern. Dieser Kaufvertrag wird als Block in der _Blockchain_ gespeichert und ist dann nicht mehr änderbar. Die Erklärung, wieso dieser Block nicht mehr änderbar ist, würde hier den Rahmen sprengen. Mit Hilfe dieses Blocks ist dann eindeutig nachvollziehbar, wer der Besitzer eines Hashes und damit einer Datei ist. Dieser Block auf der _Blockchain_ ist es, was nun neuerdings "NFT" genannt wird. Im Prinzip identifiziert dieser Block nun die Datei und ihren Besitzer - ist also ein nicht austauschbarer Token für die Verbindung zwischen Hash und Käufer.

### Wozu die Blockchain?

Das ist eine gute Frage :) Man könnte auch einfach den Kaufvertrag über eine Online-Handelsplattform wie bspw. Ebay abschließen. Zwei "Probleme" die hierbei scheinbar auftauchen sind:

- dass man der Plattform (einer zentralen Institution) vertrauen müsste, diese Verträge rechtlich bindend zu verifizieren
- dass man nicht anonym ist

Beide Probleme werden durch die _Blockchain_ gelöst; man kann damit _anonyme_ Kaufverträge abschließen und diese _dezentral_ verifizieren. Technisch ist das meiner Meinung nach hochinteressant. Jedoch kann man sich schon fragen, ob diese beiden Punkte bei Kaufverträgen wirklich kritische Probleme darstellen, denn zumindest die Anonymität ist nicht zwangsläufig gewährleistet. Schließlich werden die meisten _Käufer_ die erworbenen Dateien (oder digitalen Güter) auf irgendwelchen Plattformen "ausstellen" oder nutzen wollen, wodurch sie in den meisten Fällen wieder identifizierbar werden dürften. Die meisten _Verkäufer_ werden den Erlös (Cryptowährung) in echtes Geld wechseln und sind dabei an die _zentrale_ Wechselstelle (Cryptobörse) gebunden, wodurch sie ebenfalls identifizierbar werden - noch dazu an einer zentralen Stelle.

### Wozu der Hash?

Wer aufmerksam gelesen hat, wird vielleicht bemerkt haben, dass man statt des Hashes einer Datei ja einfach direkt die Datei selbst verkaufen und in dem Block auf der _Blockchain_ speichern kann. Theoretisch ist das möglich, würde aber schnell dazu führen, dass die _Blockchain_ riesige Speichermengen benötigen würde, da sie global vorgehalten werden muss und jeder Block immer verfügbar sein muss; die Kette wächst immer nur und nichts darf gelöscht werden (die Erklärung hierfür würde den Rahmen sprengen). Würde man nun bspw. mehrstündige 4K-Filme in den Blöcken ablegen, würde das schnell zu riesigen Speichermengen führen. Hashes sind hier ein gutes Mittel, da sie immer eine feste Länge haben, der Hash eines mehrstündigen 4K-Films ist genauso lang, wie der obige Hash "_5b55704f60c550fc594c65d5e3032b10eee43eeb_" des kleinen Bildes. Dass nur die Hashes in des Blöcken gespeichert werden, bringt allerdings andere Probleme mit sich, auf die ich hier aber nicht näher eingehen werde.
