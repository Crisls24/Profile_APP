# Profile App — Currículum con Mapa

Perfil profesional / CV interactivo en Android, hecho con **Jetpack Compose**: photografía,
datos de contacto, lista de lenguajes y una descripción personal, con un **mapa de Google**
que ubica la meta profesional.

## Stack

- **App:** Kotlin 2.0.21 + Jetpack Compose (Material 3).
- **Mapa:** Google Maps Compose (`maps-compose:6.0.0`) + `play-services-maps:18.2.0`.
- Pantalla única (un solo Activity), sin navegación adicional.

## Funcionalidades

- Diseño de perfil: portada, foto, nombre, correo y descripción.
- Sección "LENGUAJES" en carrusel horizontal (Kotlin, Java, Python, Swift, Dart, etc.).
- **Google Map** con marcador en la ubicación profesional objetivo y zoom configurable.
- Botón flotante de acciones adicionales (en desarrollo).

## Configuración del mapa

La API key de Google Maps se lee desde `local.properties` (no se sube a git):

```properties
# local.properties
sdk.dir=C:\\Users\\tuUsuario\\AppData\\Local\\Android\\Sdk
MAPS_API_KEY=AIzaSyTuClaveDeGoogleMapsAqui
```

> Crea tu key desde Google Cloud Console (Maps SDK for Android) y restringe el acceso
> por package (`com.sys.cursokotlin.profile_app`) y SHA-1. Hay una plantilla en
> `local.properties.example`.

## Cómo ejecutar

Abrir con **Android Studio** y ejecutar el módulo `app` (Gradle wrapper, Java 17).

## Soporte

Android 7.0+ (minSdk 24), targetSdk 35. Requiere conexión a internet para cargar el mapa.