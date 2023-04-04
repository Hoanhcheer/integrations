# createIntegration

The `createIntegration()` method is the main entry point for your app or integration. It provides the context for GitBook around how your app should look and behave.

The `createIntegration()` method can take 4 optional arguments, and must be exported from the main script executed in your app's `gitbook-manifest.yaml` file. See the [Configurations section](../configurations.md) for more info.

| Argument     | Description                                                                                                            |
| ------------ | ---------------------------------------------------------------------------------------------------------------------- |
| `fetch`      | An async fetch event used to communicate with the GitBook API to make requests.                                        |
| `events`     | Handler for GitBook events.                                                                                            |
| `components` | The component(s) to expose in your integration. See the [`createComponent`](createcomponent.md) section for more info. |

### Example

```typescript
export default createIntegration({
    fetch: async () => {},
    components: [createComponent(options)],
    events: {},
});
```