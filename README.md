```
                         _               _       _       ____
              _   _ _ __| |_      ____ _| |_ ___| |__   |___ \
             | | | | '__| \ \ /\ / / _` | __/ __| '_ \    __) |
             | |_| | |  | |\ V  V / (_| | || (__| | | |  / __/
              \__,_|_|  |_| \_/\_/ \__,_|\__\___|_| |_| |_____|

                                  ... monitors webpages for you
```

DEMO: Running [urlwatch](https://github.com/thp/urlwatch) on github with [github actions](https://github.com/huwan/urlwatch-actions-demo/actions)

urlwatch config files:
 - `urlwatch.yaml`: config file, e.g., set up e-mail sending
 - `urls.yaml`: job lists
 - `.github/workflows/main.yml`: github action workflow

This demo shows:
 - Install dependencies and setup urlwatch;
 - Use action secrets to pass password to workflow;
 - Run urlwatch workflow when specific activity on GitHub happens (e.g., push), at a scheduled time (using posix cron syntax), or you can manually trigger workflow runs;
 - Store workflow data, i.e., database file for change history, as workflow artifact.

**Caution**: This demo uses [app password](https://urlwatch.readthedocs.io/en/latest/reporters.html#smtp-login-without-keyring) for [e-mail reporter (via gmail)](https://urlwatch.readthedocs.io/en/latest/reporters.html#e-mail-via-gmail-smtp) in urlwatch.yaml file. To prevent password leaks, use a private github repository or use [encrypted secrets](https://docs.github.com/en/actions/reference/encrypted-secrets) (create a repository secret GMAIL_APP_PASSWORD for gmail reporter) if you want to run urlwatch via github actions.

