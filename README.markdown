# my snippets

I created this repository just because I do not like the Gist interface, and
Pastebin do not have version control.

files:

  * `Makefile`: user defined functions I may use in the future

  * `storage-test.bash`: tests whether a storage device (such as an SD card) is
    broken, by store something in, and fetch them out. The card should contain
    enough space for the test. It accepts these options (passed in as
    environment variables):
      * `$CARD`: _required_ directory of the card, mounted.
      * `$NUM`: number of files, each sized one gigabytes. Defaults to 20.
      * `$FOLDER`: the folder to store the files, both in current directory and
        in the card. Defaults to `'test-files'`.
      * `$LOG_FILE`: the log file. Defaults to `'log'`. You may want it be
        `/dev/null`.

  * `push-or-show.bash`: build and push Docker image to Docker Hub, or show
    logs on failure. Require [Semaphore](https://semaphoreci.com/) specific
    [`docker-cache`](https://semaphoreci.com/docs/docker.html).
