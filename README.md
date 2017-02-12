# Muscovy

Muscovy is (or will be) a tool for editing TEI schemas (ODD files).

Muscovy is an XForm which uses the TEI Consortium's OxGarage service to perform conversions.

Currently Muscovy allows a user to upload an existing ODD file to OxGarage, validating it, and having done so, to generate a RelaxNG schema from it. It does not yet provide any interface for editing the specification.

To run, check out the repository into a folder on a web server. Access the index.xhtml file via a web browser.

Muscovy is constrained by browser security settings. Because the TEI Consortium's OxGarage service is not currently configured to allow Cross Origin Resource Sharing, the XForm will be unable to communicate with it. To work around this, it's recommended to install a browser extension such as Chrome's [ForceCORS](https://chrome.google.com/webstore/detail/forcecors/oajaiobpeddomajelicdlnkeegnepbin) to spoof the CORS headers. Once installed, open ForceCORS by clicking the padlock icon on the Chrome toolbar, add a URL pattern `http://www.tei-c.org/ege-webservice/*` and add the following headers and values:


| Header Name                   | Header Value         |
| ----------------------------- | -------------------- |
| Access-Control-Allow-Headers  | Content-Type         |
| Access-Control-Allow-Origin   | *                    |
| Access-Control-Expose-Headers | Content-Disposition  |

Click the green "Save All" button.
