# platinumplace/laravel-dgii-xml-signer

[![Latest Version on Packagist](https://img.shields.io/packagist/v/platinumplace/laravel-dgii-xml-signer)](https://packagist.org/packages/platinumplace/laravel-dgii-xml-signer)

Un firmador de XML conforme al estándar de la DGII (República Dominicana) para aplicaciones Laravel.

## Requisitos

* PHP ^8.4
* Laravel Framework ^12.0
* Extensión DOM (`ext-dom`)
* Extensión OpenSSL (`ext-openssl`)

## Instalación

1. En tu proyecto Laravel, instala el paquete via Composer:

```bash
   composer require platinumplace/laravel-dgii-xml-signer
```
   
## Uso Básico

```php
use DGII\Signer\DGIISigner;

$xml = file_get_contents(base_path('factura.xml'));
$certStore = file_get_contents(base_path('certificado.p12'));
$password = 'password';

$signed = DGIISigner::sign($certStore, $password, $xml);
```

## Soporte de Dependencias

Internamente utiliza [selective/xmldsig](https://github.com/selective-php/xmldsig) para el procesamiento de firmas:

```json
"require": {
    "selective/xmldsig": "^3.1"
}
```

## Contribuciones

1. Haz un *fork* del repositorio.
2. Crea tu rama de funcionalidad (`git checkout -b feature/nueva-funcion`).
3. Realiza *commit* de tus cambios (`git commit -m 'Agrega nueva función'`).
4. Sube a tu repositorio (`git push origin feature/nueva-funcion`).
5. Abre un Pull Request.

## Licencia

MIT © \[Tu Nombre o Empresa]

---

Para más detalles de cómo funciona y por qué deben visitar el repositorio original: [https://github.com/platinum-place/php-dgii-xml-signer?tab=readme-ov-file#php-dgii-xml-signer](https://github.com/platinum-place/php-dgii-xml-signer?tab=readme-ov-file#php-dgii-xml-signer)
