# MuleSoft Cloudmersive Virus Scan API Call Example

![image](https://github.com/user-attachments/assets/3b6e0bd9-0806-4304-b453-27cbd2f92770)

In this example, a base-64 encoded input is taken in this format:

```
{
  "encodedData": "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"
}
```

This input is decoded and then sent to the Cloudmersive Advanced Virus Scanning API.  This produces an output like this after calling the Cloudmersive API:

```
{
    "CleanResult": true,
    "ContainsExecutable": false,
    "ContainsInvalidFile": false,
    "ContainsScript": false,
    "ContainsPasswordProtectedFile": false,
    "ContainsRestrictedFileFormat": false,
    "ContainsMacros": false,
    "ContainsXmlExternalEntities": false,
    "ContainsInsecureDeserialization": false,
    "ContainsHtml": false,
    "ContainsUnsafeArchive": false,
    "ContainsOleEmbeddedObject": false,
    "VerifiedFileFormat": ".xlsx",
    "FoundViruses": null,
    "ContentInformation": {
        "ContainsJSON": false,
        "ContainsXML": false,
        "ContainsImage": false,
        "Hash_SHA1": "2JH87vR6+f7C1T5B0Y6aiH/V1rc=",
        "RelevantSubfileName": null,
        "RelevantSubfileHash_SHA1": null,
        "IsAuthenticodeSigned": false
    }
}
```

Be sure to set your API key in `muletest2.xml` along with your API endpoint if you do not wish to use Public Cloud.
