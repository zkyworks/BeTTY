# BeTTY

A new local-first Internet protocol based on gopher, Plan 9 From Bell Labs,  and the data lakehouse model. It uses JSON files called *bettyDocs* to store information in a human- and machine-readable format.

## Software

BeTTY is made up of several components:

* **bettyd** - the BeTTY daemon, which reads and writes JSON files using your designated storage backend. It uses public/private key encryption to handle authorization and authentication instead of passwords and TLS/SSL. This is the only necessary component to use BeTTY; all the others are ways to make it easier to work with bettyDocs.
* **btty** - a command-line utility which interfaces with bettyd, automatically handling things like *encryption*, *indexing*, and *transclusion*.
* **httbd** - a web gateway for BeTTY which uses *btty* on the backend. It uses marXDown to present bettyDocs in XHTML (and of course, Markdown).
* **marXDown** - a Markdown format for bettyDocs with a variety of useful *dialects* which help you organize topics into shareable documents.
