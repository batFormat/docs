# Интеграция с сервисами {{ yandex-cloud }}

Вы можете использовать сертификаты из {{ certificate-manager-name }} в следующих сервисах {{ yandex-cloud }}:
* [{{ objstorage-full-name }}](#os).
* [{{ api-gw-full-name }}](#api-gw).

## {{ objstorage-full-name }} {#os}

Если бакет используется для хостинга статического сайта, [используйте сертификат](../../storage/operations/hosting/certificate.md#cert-manager) из {{ certificate-manager-name }} для доступа к сайту по протоколу `HTTPS`. При изменении сертификата в {{ certificate-manager-name }}, он будет автоматически обновлен во всех использующих его бакетах.

{% note warning %}

* Доступ к бакету по `HTTPS` открывается в течение получаса после выбора сертификата.
* Применение изменений сертификата также может занимать до получаса.

{% endnote %}

## {{ api-gw-full-name }} {#api-gw}

{{ api-gw-full-name }} позволяет объединить несколько микросервисов в единый продукт. Микросервисы могут быть запущены в виртуальных машинах, контейнерах или реализованы в виде функций. Вы сможете использовать домен для обращения к API.

Для обеспечения TLS-соединения будет использован привязанный к домену сертификат.

#### См. также {#see-also}

- [Статический веб-сайт в {{ objstorage-name }}](../../solutions/web/static.md)
- [{{ api-gw-full-name }}](../../api-gateway/index.yaml)