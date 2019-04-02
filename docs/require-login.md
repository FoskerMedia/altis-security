# Require Login

By default, all websites are publicly accessible. In some situations, you may want to require users be logged in to access the website. This is especially useful when in pre-launch mode.

Environments running in Cloud that are not of type `production` have the `require-login` feature enabled by default. Set the `platform.require-login` setting to `true` to require all users be logged in to view the website. If you want to make a non-production site public, set the `platform.environments.${ environment-name }.require-login` setting to `false`.

```json
"platform": {
	"modules": {
		"security": {
			"require-login": true
		}
	},
	"environments": {
		"local": {
			"modules": {
				"security": {
					"require-login": false
				}
			}
		}
	}
}
```
