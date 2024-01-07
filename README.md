<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="author" content="Mateusz">
    <meta name="description" content="DNS">        
</head>
<body>
    <h1>Learn DNS with me!</h1>
    <ol>
        <li>
            <h2>Czym jest DNS?</h2>
            <p><strong>DNS (Domain Name System)</strong> - system serwerów, protokół komunikacyjny i usługa konwertująca adresy znane użytkownikom Internetu na adresy zrozumiałe dla urządzeń tworzących sieć komputerową. Usługa DNS jest powiązana z portem TCP/UDP 53.</p>
            <p>Adresy DNS składają się z domen internetowych rozdzielonych kropkami. W ten sposób możliwe jest budowanie hierarchii nazw, które porządkują Internet.</p>
            <hr>
            <h2>DNS oparty jest na modelu drzewa odwróconego.</h2>
            #img 
            <hr>
        </li>
        <li>
            <h2>Zapytania DNS</h2>
            <h4>DNS dzielimy na dwa rodzaje zapytań</h4>
            <ul>
                <li><strong>Rekurencyjne -</strong> zmusza serwer do znalezienia wymaganej informacji lub zwrócenia wiadomości o błędzie. Ogólną zasadą jest, że zapytania od resolwera (program, który potrafi wysyłać zapytania do serwerów DNS) do serwera są typu rekurencyjnego, czyli resolwer oczekuje podania przez serwer adresu IP poszukiwanego hosta. Wykonywanie zapytań rekurencyjnych pozwala wszystkim uczestniczącym serwerom zapamiętać odwzorowanie (ang. DNS caching), co podnosi efektywność systemu.</li>
                <li><strong>Iteracyjne -</strong> wymaga od serwera jedynie podania najlepszej dostępnej mu w danej chwili odpowiedzi, przy czym nie musi on łączyć się jeszcze z innymi serwerami. Zapytania wysyłane pomiędzy serwerami są iteracyjne, przykładowo wiarygodny serwer domeny org nie musi znać adresu IP komputera www.pl.wikipedia.org, podaje więc najlepszą znaną mu w tej chwili odpowiedź, czyli adresy serwerów autorytatywnych dla domeny wikipedia.org</li>
            </ul>
            <hr>
        </li>
        <li>
            <h2>Odpowiedzi DNS</h2>
            <h4>DNS posiada dwa rodzaje odpowiedzi</h4>
            <ul>
                <li><strong>Autorytatywne -</strong> dotyczące domeny w strefie, nad którą dany serwer ma zarząd, pochodzą one bezpośrednio z bazy danych serwera; jest to pozytywna odpowiedź zwracana do klienta, która w komunikacie DNS zawiera ustawiony bit uwierzytelniania (AA- Authoritive Answer) wskazujący, że odpowiedź została uzyskana z serwera dokonującego bezpośredniego uwierzytelnienia poszukiwanej nazwy.</li>
                <li><strong>Nieautorytatywne -</strong> dane które zwraca serwer pochodzą spoza zarządzanej przez niego strefy; odpowiedzi nieautorytatywne są buforowane przez serwer przez czas TTL, wyspecyfikowany w odpowiedzi, później są usuwane.</li>
            </ul>
            <hr>
        </li>
        <li>
            <h2>Rekordy DNS</h2>
            <h4>Opis domeny dokonywany jest przy użyciu tzw. rekordów zasobowych DNS. Przykłady rekordów:</h4>
            <ul>
                <li><strong>rekord A lub rekord adresu IPv4 -</strong> mapuje nazwę domeny DNS na jej 32-bitowy adres IPv4.</li>
                <li><strong>rekord AAAA lub rekord adresu IPv6 -</strong> mapuje nazwę domeny DNS na jej 128-bitowy adres IPv6.</li>
                <li><strong>rekord CNAME lub rekord nazwy kanonicznej -</strong> ustanawia alias nazwy domeny.</li>
                <li><strong>rekord MX lub rekord wymiany poczty -</strong> mapuje nazwę domeny DNS na nazwę serwera poczty.</li>
                <li><strong>rekord PTR lub rekord wskaźnika -</strong> mapuje adres IPv4 lub IPv6 na nazwę kanoniczną hosta.</li>
                <li><strong>rekord NS lub rekord serwera nazw -</strong>  mapuje nazwę domenową na listę serwerów DNS dla tej domeny.</li>
                <li><strong>rekord SOA lub rekord adresu startowego uwierzytelnienia -</strong>  ustala serwer DNS dostarczający autorytatywne informacje o domenie internetowej.</li>
                <li><strong>rekord TXT -</strong> pozwala dołączyć dowolny tekst do rekordu DNS.</li>
            </ul>
            <hr>
        </li>
        <li>
            <h2>Podział domen głównego poziomu</h2>
            <ul>
                <li>Domeny geograficzne</li>
                <p>Przykłady:</p>
                <ul>
                    <li>.pl - Polska</li>
                    <li>.us - Stany Zjednoczone</li>
                    <li>.uk - Wielka Brytania</li>
                    <li>.tw - Taiwan</li>
                    <li>.eu - Europa</li>
                </ul>
                <li>Domeny organizacyjne</li>
                <p>Przykłady:</p>
                <ul>
                    <li>.com - firmy komercyjne</li>
                    <li>.edu - instytucje naukowe</li>
                    <li>.gov - agencje rządowe</li>
                    <li>.mil - organizacje wojskowe</li>
                    <li>.net - związane z siecią Internet</li>
                    <li>.int - międzynarodowe organizacje rządowe i pozarządowe</li>
                    <li>.org - pozostałe organizacje</li>
                </ul>
            </ul>
            <hr>
        </li>
        <li>
            <h2>Organizacja zarządzająca DNS</h2>
            <p>Organizacją zajmującą się zarządzaniem przestrzenią nazw domenowych jest ICANN (The Internet Corporation for Assigned Names and Numbers).</p>
        </li>
        <hr>
    </ol>
    <h2>Koniec materiału, dziękuję za uwagę :)</h2>
</body>
</html>
