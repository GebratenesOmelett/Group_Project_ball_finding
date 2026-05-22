# Ball Tracking

`track_ball.py` poprawia wykrywanie małej piłki przez:

- większy model i większe `imgsz` dla pełnej klatki,
- dodatkowe wyszukiwanie w powiększonym ROI wokół predykcji Kalmana,
- niższy próg `min_box_area` dla bardzo małych detekcji,
- poprawkę logiki Kalmana: predykcja jest liczona raz na klatkę, nie raz na każdy box.

Uruchomienie:

```powershell
python .\track_ball.py
```

Tryb bez okna podglądu:

```powershell
python .\track_ball.py --hide-window --max-frames 300
```

Zapis wyniku do pliku:

```powershell
python .\track_ball.py --output tracked.mp4
```
