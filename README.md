# FuneralPhoto Windows Releases

Publiczny kanal aktualizacji aplikacji FuneralPhoto Windows.

Aplikacja Windows pyta Supabase Edge Function `app-version` z parametrem `platform=windows`. Edge Function wybiera najnowszy GitHub Release z tego repo i szuka assetu pasujacego do wzorca:

```text
FuneralPhoto-Windows-*
```

Publikuj paczki Windows jako np.:

```text
FuneralPhoto-Windows-1.0.0-x64.zip
FuneralPhoto-Windows-1.0.0-x64.msi
FuneralPhoto-Windows-1.0.0-x64.msix
```

To repo jest tylko dla Windows. Paczki macOS publikuj w osobnym kanale macOS, zeby aplikacje nie pobieraly nieprawidlowych aktualizacji.
