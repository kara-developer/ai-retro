# Yapay zekana her hafta kendi hatalarını incelet

Yapay zekan aynı hatayı iki kere yapıyorsa sorun hafızada: düzelttiğin şey bir sonraki sohbette unutuluyor. Bu yöntemde haftada bir yapay zeka **geçen haftaki düzeltmelerini** tarar ve her birini **kalıcı kurala** çevirir. Küçük şeyleri kendi düzeltir, büyük değişikliği sana öneri olarak getirir.

## Ne lazım
- Yapay zekanın her işte okuduğu bir **kurallar dosyası** (Claude Code'da `CLAUDE.md`, ChatGPT'de "Özel talimatlar"/proje talimatı).
- Geçen haftanın izi: sohbet geçmişi, not dosyası ya da günlük (ne kadar varsa).

## Nasıl çalışır
1. Haftada bir (ör. Pazartesi sabahı) `PROMPT.md`'yi çalıştır. Claude Code'da zamanlanmış görev olarak kendiliğinden de çalışabilir.
2. Yapay zeka son 7 günü tarar: **nerede düzeltildi, ne unutuldu, ne iki kere oldu.**
3. Her bulgu için risk ayrımı:
   - **Küçük** (bir kural cümlesi eklemek, yazım düzeltmek) → kendisi uygular.
   - **Büyük** (çalışma şeklini değiştiren, bir şeyi silen) → sana öneri olarak gelir.
4. Haftada **en fazla 3 öneri**, en çok sorun çıkaran konudan başlayarak. Öneri yağmuru olmaz.

## Örnek
Yapay zeka saatleri yanlış saat diliminde söylüyordu. Retro bunu yakaladı, kurallara "saatleri hep Türkiye saatiyle söyle" eklendi. Bir daha olmadı.

`PROMPT.md` → yapay zekana yapıştır.
