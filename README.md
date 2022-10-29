# discord_protos

Protocol files constructed by hand from Discord's web client files.

They have been put under `discord_protos.discord_users.v1.*` as indicated
by the client, although the protocol messages and enums have been split
across individual files, since Discord uses [`protobuf-ts`](https://github.com/timostamm/protobuf-ts)
there may actually be just 2 files, i.e. one for frecency and another for
preloaded settings (assuming by protobuf-ts' proto compiling).

These are the protobuf(s) returned by the `/users/@me/settings-proto/{1|2|3}`
API endpoint.

> info
> All the materials in this repository are for educational purposes only.

## Endpoint mappping to proto file

As mentioned in [`settings_proto_types.json`](./settings_proto_types.json)
there are 3 types of *settings-proto*

- `1`: `PRELOADED_USER_SETTINGS`, which is [`preloaded_user_settings.proto`](./discord_protos/discord_users/v1/preloaded_user_settings.proto)
- `2`: `FRECENCY_AND_FAVORITES_SETTINGS`, which is [`frecency_user_settings.proto`](./discord_protos/discord_users/v1/frecency_user_settings.proto)
- `3`: `TEST_SETTINGS`, which does not have any public facing proto definitions,
  at least not in the client
