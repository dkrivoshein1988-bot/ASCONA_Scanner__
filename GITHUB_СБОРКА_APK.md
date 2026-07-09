# Сборка APK через GitHub

На текущем ПК нет Flutter, Dart, Java и Android SDK, поэтому APK удобнее собирать через GitHub Actions.

## Новый репозиторий проекта

Загрузите в корень нового GitHub-репозитория содержимое папки:

```text
ascona_returns_android
```

В корне репозитория должны лежать:

```text
README.md
pubspec.yaml
analysis_options.yaml
GITHUB_СБОРКА_APK.md
lib/main.dart
.github/workflows/build_android.yml
```

## Сборка APK в GitHub Actions

1. Откройте вкладку `Actions`.
2. Выберите `Build Android APK`.
3. Нажмите `Run workflow`.
4. После завершения скачайте артефакт:

```text
ascona-returns-apk
```

Внутри будет:

```text
app-release.apk
```

## Если workflow не появился

Проверьте, что файл загружен именно по пути:

```text
.github/workflows/build_android.yml
```

Если папка `.github` не попала в репозиторий при загрузке архива, создайте файл вручную через GitHub:

```text
Add file -> Create new file -> .github/workflows/build_android.yml
```

