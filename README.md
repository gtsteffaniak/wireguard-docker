# Wireguard docker-compose

For secure and fast home VPN access - to access all your local-only resources
from anywhere.

## How to run

**Prereqs**:

 * docker
 * docker-compose

**starting the program**:

 1) Update docker-compose file with your own information! `dns`, `public ip`,
    and maybe the `TZ`.
   * public ip needs to have port forward from your gateway/router to whatever
     device you are running wireguard on.
   * Timezone is [TZ format](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).
 1) Navigate terminal to the directory with `docker-compose.yml`
 1) Run `docker-compose up` to test while sending logs to console.
    * Take note of any peer keys that get generated in output.
 1) CTL+C once to gracefully shutdown once you are done testing.
 1) you should see new folder `config/` with your custom config.
 1) Run permantently even after reboot with `docker-compose up -d`
