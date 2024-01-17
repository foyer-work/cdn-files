# CDN Files served using JSDelivr

Use this repo to store files which are to be served by the JSDelivr CDN. This repo is **PUBLIC**, so **DO NOT** include files which have sensitive information related to Merlin, or Foyer or any other production service in deployment.

### Example URL

File Name: `merlin_config.json`

CDN URL: `https://cdn.jsdelivr.net/gh/foyer-work/cdn-files@latest/merlin_config.json`

### Purge Cache from CDN

**NOTE:** DO NOT PURGE MULTIPLE TIMES IN A ROW TO AVOID GETTING RATE LIMITED ON THE PURGE API. ALSO CHECK THE FORMATTING OF THE JSON BEFORE PURGING.
**NOTE:** IF IN DOUBT, DO NOT YOLO IT, ASK BEFORE TAKING ANY ACTION.

1. Tag the specific commit to the latest version according to the semver convention as `git tag ${semver} && git push origin ${semver}`.
3. Head to `https://jsdelivr.com/tools/purge`.
4. Enter upto 10 JSDelivr URLs of the files to be purged.
5. Click Purge and test out the URL again to check if the file has been updated.
