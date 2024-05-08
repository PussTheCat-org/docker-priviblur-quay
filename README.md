# docker-priviblur-quay

A [Priviblur](https://github.com/syeopite/priviblur) image, on Quay.

[Quay page](https://quay.io/repository/pussthecatorg/priviblur) | [GitHub page](https://github.com/PussTheCat-org/docker-priviblur-quay)

This image mostly exist for the [PussTheCat.org](https://pussthecat.org/) [instance](https://priviblur.pussthecat.org/), but others are free to use it.

## Usage:

- Download (or copy the content of) the `docker-compose.yml` 
- Download (or copy the content of) the `config.toml` from this repository, or from upstream: https://github.com/syeopite/priviblur/blob/master/config.example.toml
- Customize the `config.toml` file how you want 
    - uncomment "url" under [cache] to enable Redis (Every other options in the [cache] section will use their default value (indicated next to them) if they are kept commented out.)
- Move both files to the folder you want
- `docker-compose up -d`
