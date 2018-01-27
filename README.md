# Heroku Buildpack: commithash

This Heroku buildpack enables deploying the current commit hash to an arbitrary path in your app.

## Usage

### Add your config variable(s):

variable | description
--- | --- 
`COMMITHASH_DEPLOY_PATH` | The relative path to deploy the commit hash to. (*Example: `public/commithash.txt`*) | 

### Add the buildpack to your Heroku app:

     heroku buildpacks:add https://github.com/tygerbytes/heroku-buildpack-commithash.git

### Example

Let's put it all together with an example. 

**Scenario**: You want to deploy the commit hash to your app's `public` directory.

     heroku config:set COMMITHASH_DEPLOY_PATH=public/commithash.txt
     heroku buildpacks:add https://github.com/tygerbytes/heroku-buildpack-commithash.git

That's it. Once you've set those config vars, your commit hash will be deployed with every build.

## License
MIT. See [LICENSE.md](LICENSE.md).
