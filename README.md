# DiveLog Converter

Statická PWA pro kontrolu dat získaných z ručně psaných potápěčských deníků a export CSV pro Diving LogBook.

## Nasazení na GitHub Pages
1. Vytvořte nový veřejný nebo soukromý repozitář.
2. Nahrajte obsah této složky do kořene repozitáře.
3. V Settings > Pages nastavte Deploy from a branch, větev `main`, složku `/ (root)`.
4. Počkejte na dokončení Pages deploymentu.

## Externí OCR
Tato verze záměrně neobsahuje API klíč. Načítá strukturovaný JSON/CSV z externího OCR a umožní data opravit. Přímé volání placeného OCR z veřejného GitHub Pages by odhalilo tajný klíč. Pro přímé napojení použijte backend/serverless proxy.

## Importní pole
`dive_number,date,location_name_ocr,location_id,location_name,country,max_depth_m,duration_min,start_time,end_time,entry_type,air_temp_c,water_temp_c,buddy,notes`

## Verze
1.0.0
