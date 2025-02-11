# Troubleshooting

Below is the list of the most frequent issues with {{ cdn-name }} and ways to resolve them.

## The CDN responds to file requests with 3xx codes (redirect)

Check that the [resource](concepts/resource.md) settings include:

* The protocol used by the origins as the primary protocol (HTTP or HTTPS). If origins redirect requests from a URI with the `http` scheme to a URI with the `https` scheme, you must select the HTTPS protocol for the resource, and vice versa.

* The value of the HTTP `Host` header from which origins don't redirect requests.

  > For example, if the header value is configured as `www.example.com`, and the origins redirect requests with this value to `example.com`, change the value in the settings to `example.com`.

## The CDN responds to file requests with 4xx codes (client error)

Make sure that:

* End-client access to the content is allowed in the resource settings.

* Origins return files in response to direct requests (bypassing the CDN).

* Origins allow and correctly process requests that match the resource settings:
  * Over the specified protocol: HTTP or HTTPS.
  * With the specified value of the `Host` HTTP header and other headers.

## CDN responds to file requests with 5xx codes (server error)

Make sure that:

* Origins respond to CDN server requests within 5 seconds.

* Origins allow and correctly process requests that match the resource settings:
  * Over the specified protocol: HTTP or HTTPS.
  * With the specified value of the `Host` HTTP header and other headers.

Check also the {{ cdn-name }} status on the [special page {{ yandex-cloud }}](https://status.cloud.yandex.ru/dashboard?service=cloud%20cdn).
