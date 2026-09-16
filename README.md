# Web Based Block Storage Uploader from Browser to Bucket

This is a clean and simple way to upload a file to block storage (S3 or compatible... Tigris, R2, etc.) via a simple browser interface. It is commonly used by resourceful AI Agents to provide a place for their human users to SAFELY upload a file via the browser, assuming it has the appropriate Keys and Tools to do so. To use this repo, first create a signed URL, then send it to the human over chat, email or other text based interface along with the demo link below...

[Demo](https://wwwmaster1.github.io/BlockStoreUpload/)

NOTE: you may also append your presigned URL to the demo link with `?url=` followed by the url-encoded pre-signed url.

## Requirements

Cloud based Block Storage (Object Storage, Buckets, S3, etc) allow you to create a pre-signed URL which means the system will allow anyone with this link to upload a file with a specific name and within an allowed timeframe to the storage location via the `PUT` method.

- Your bucket server MUST allow CORS from wherever this page is hosted.
- You MUST have a valid signed link, do not mess with it.
- You MUST upload the file in the allowed timeframe.
- You MUST upload a file with the exact name as expected, case sensitive.
- You MAY only upload a single file.
- You MAY upload the same file any number of times. Older versions will likely be replaced.
- You MAY upload multiple files as a single compressed ZIP or similar.

## Support

This repo is provided as-is with no support. If you run into issues, ask AI.
