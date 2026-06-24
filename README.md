# FuneralPhoto Windows Releases

Publiczny kanał aktualizacji aplikacji FuneralPhoto Windows.

Aplikacja Windows pyta Supabase Edge Function `app-version` z parametrem `platform=windows`. Edge Function najpierw próbuje odczytać najnowszy GitHub Release z tego repo, a jeżeli release jeszcze nie istnieje, używa manifestu `windows-update.json` z gałęzi `main`.

## GitHub Release assets

Preferowany sposób publikacji aktualizacji to GitHub Release z assetem pasującym do wzorca:

```text
FuneralPhoto-Windows-*
```

Przykłady nazw:

```text
FuneralPhoto-Windows-1.0.0-x64.zip
FuneralPhoto-Windows-1.0.0-x64.msi
FuneralPhoto-Windows-1.0.0-x64.msix
```

## Manifest fallback

`windows-update.json` jest publicznym feedem awaryjnym dla Windows. Zawiera wersję, URL paczki, SHA-256 i notatki wydania. Dzięki temu Windows nie korzysta z macOS-owego repo release.

To repo jest tylko dla Windows. Kod aplikacji Windows jest w prywatnym repo `funeralphoto-windows`; paczki macOS publikuj w osobnym kanale macOS.
