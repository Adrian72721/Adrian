Voi folosi SQL (PostgreSQL) pentru a rezolva această problema.

Am folosit website_domain ca principal criteriu deoarece este în general unic pentru fiecare companie
Am inclus company_legal_names și main_country_code pentru a distinge companii cu nume de domeniu similar din diferite țări
STRING_AGG este utilizat pentru a aduna toate variantele numelor comerciale într-un singur câmp
MIN(company_name) ia prima variantă a numelui companiei 
MIN(created_at) și MAX(last_updated_at) retin intervalul temporal al înregistrărilor

In final companiile sunt afisate o singura data si sunt păstrate în câmpul company_commercial_names
