# DFTooling Resource Pack Repository
The DFTooling resource pack repositories stores resourcepacks that plots use on the DiamondFire server.

## Add a pack

### Using the [FireClient](https://modrinth.com/mod/fireclient) mod

1. Make sure the pack is located in your Minecraft instance's `resourcepacks` folder.
2. Run `/uploadpack <filename>` to upload the pack. It automatically zips folders before upload. You must quote your filename if it contains a space.

### Using the [DFTooling API](https://api.dftooling.dev/docs)

Make a `POST` request to `https://api.dftooling.dev/api/packs/v0/upload`, passing the `token` parameter containing the auth token, and the raw bytes of the pack zip in the request body. A json object will be returned, if the request was successfull there will be a `url` key containing the URL to the uploaded pack.

You **must** be authenticated with the API to interact with this endpoint. See the [API docs](https://api.dftooling.dev/docs) for more information.
