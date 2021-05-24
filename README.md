```
                         _               _       _       ____
              _   _ _ __| |_      ____ _| |_ ___| |__   |___ \
             | | | | '__| \ \ /\ / / _` | __/ __| '_ \    __) |
             | |_| | |  | |\ V  V / (_| | || (__| | | |  / __/
              \__,_|_|  |_| \_/\_/ \__,_|\__\___|_| |_| |_____|

                                  ... monitors webpages for you
```

DEMO: Running urlwatch on github with github actions

urlwatch config files:
 - `urlwatch.yaml`: config file, e.g., set up e-mail sending
 - `urls.yaml`: job lists
 - `.github/workflows/main.yml`: github action workflow

This demo shows:
 - Install dependencies and setup urlwatch
 - Run urlwatch workflow when specific activity on GitHub happens (e.g., push), at a scheduled time (using posix cron syntax), or you can manually trigger workflow runs.
 - Store workflow data, i.e., database file for change history, as workflow artifact.

**Caution**: This demo use cleartext app password for e-mail reporter in urlwatch.yaml file. To prevent password leaks, use a private github repository.
