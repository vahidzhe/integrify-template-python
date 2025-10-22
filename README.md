# Integrify Template

Bu reponu istifadə etməklə yeni inteqrasiyaları yaradıb, ekosistemə uyğun alt-kitabaxanalar yaratmaq asanlaşır.

Addımlar:

1. Reponun sağ yuxarı küncündə "Use this template -> Create new repository"
2. Lokalınıza yükləyin - `git clone git@github.com:Integrify-SDK/integrify-template-python.git`
3. `python create_local_configs.py` skriptini run edin
4. `integration_name` qovluğunu işləyəciyniz inteqrasiyanın adına dəyişin
5. Ümumi axtarış verib, `{replace}` string-ini axtarın, və həmin yerləri dəyişin
6. `pre-commit` və `uv` istifadə edin
7. `uv sync` istifade etdikdən sonra, `make` əmrlərindən istifadə edə bilərsiniz
