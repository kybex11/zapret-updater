# Внимание!
Репозиторий для автономного обновления Zapret (evelentdev). Reverse-Engineering запрещён. См. LICENSE.

# zapret-updater

Пакеты **AES-256-GCM** (не `.exe`). `version.toml` подписан **Ed25519**.

## Файлы

- `version.toml` — version, sha256, sig
- `releases/*.zpk` — шифротекст

## Клиент

1. Проверка `sig`  
2. Скачивание `.zpk`, проверка sha256  
3. Расшифровка внутри `zapret.exe`  
4. Установка + перезапуск  

## Maintainer

Не коммитить `zapret-rs/secrets/ed25519.sk`.

```bat
cd zapret-rs
update.bat
```
