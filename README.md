# Web Based Object Storage Uploader (Browser to Bucket)

This is a clean and simple way to upload a file to object storage (S3 or compatible... Tigris, R2, etc.) via a simple browser interface. It is commonly used by resourceful AI Agents to provide a place for their human users to SAFELY upload a file via the browser, assuming it has the appropriate Keys and Tools to do so. To use this repo, first create a signed URL, then send it to the human over chat, email or other text based interface along with the demo link below...

[Demo](https://wwwmaster1.github.io/BLOBDrop/)

NOTE: you may also append your presigned URL to the demo link with `?url=` followed by the url-encoded pre-signed url.

```
https://wwwmaster1.github.io/BLOBDrop/?url=https%3A%2F%2Fbucket.fly.storage.tigris.dev%2Fuploads%2Ffrom-user%2Fuserfile.png%3FX-Amz-Algorithm%3DAWS4-HMAC-SHA256%26X-Amz-Content-Sha256%3DUNSIGNED-PAYLOAD%26X-Amz-Credential%3Dtid_zPYOElPNwejdiwefieWEedwEbNiJ%252F20260916%252Fauto%252Fs3%252Faws4_request%26X-Amz-Date%3D20260916T223508Z%26X-Amz-Expires%3D1800%26X-Amz-Signature%3D0c323e4064019ada87c9d5aa9ea0aa225b0961fe5d51660f8a3386a31125fd08%26X-Amz-SignedHeaders%3Dhost%26x-id%3DPutObject
```

```HTML
<A HREF="https://wwwmaster1.github.io/BLOBDrop/?url=https%3A%2F%2Fbucket.fly.storage.tigris.dev%2Fuploads%2Ffrom-user%2Fuserfile.png%3FX-Amz-Algorithm%3DAWS4-HMAC-SHA256%26X-Amz-Content-Sha256%3DUNSIGNED-PAYLOAD%26X-Amz-Credential%3Dtid_zPYOElPNwejdiwefieWEedwEbNiJ%252F20260916%252Fauto%252Fs3%252Faws4_request%26X-Amz-Date%3D20260916T223508Z%26X-Amz-Expires%3D1800%26X-Amz-Signature%3D0c323e4064019ada87c9d5aa9ea0aa225b0961fe5d51660f8a3386a31125fd08%26X-Amz-SignedHeaders%3Dhost%26x-id%3DPutObject">Upload The File</A>
```

## Requirements

Cloud based Block Storage (Object Storage, Buckets, S3, etc) allow you to create a pre-signed URL which means the system will allow anyone with this link to upload a file with a specific name and within an allowed timeframe to the storage location via the `PUT` method.

- Your bucket server MUST allow CORS from wherever this page is hosted.
- User MUST have a valid signed link, do not mess with it.
- User MUST upload the file in the allowed timeframe.
- User MUST upload a file with the exact name as expected, case sensitive.
- User MAY only upload a single file.
- User MAY upload the same file any number of times. Older versions will likely be replaced unless you have versioning enabled.
- User MAY upload multiple files as a single compressed ZIP or similar.

## Support

This repo is provided as-is with no support. If you run into issues, ask AI.

## Extending

While the file sharing method described on this page is intended to work for a single file with a specific name, it is likely possible to extend it to allow the transmission of any file (name or type) by masking the name and `Content-Type` with javascript. Further, while it is intended for a one-time upload by a single user, it is likely possible to share the link with numerous people so that each may upload a different file, if you have a versioning mechanism to gather each upload separately. Either way, use with caution.

fin.
