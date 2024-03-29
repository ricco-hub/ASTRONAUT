# ACTeroids Database

The ACTeroids Database provides users with computer-readable data for specific asteroids in the solar system. This database contains thermal emission flux data collected by the Atacama Cosmology Telescope (ACT) in the frequency bands 90, 150, and 220 GHz across three separate ACT arrays. Additionally, the database contains time (unix) of observations and flux error bars. This data is based on the paper by [Orlowski-Scherer et al. 2023](https://arxiv.org/pdf/2306.05468).

## Example Queries
- `s3://cornell-acteroids/Bamberga_lc_pa6_150.fits`
- `s3://cornell-acteroids/Bamberga_lc_pa5_150.fits`
- `s3://cornell-acteroids/Vesta_lc_pa4_220.fits` 

## Query Parameters

The general form for making a query to the S3 path is `s3://cornell-acteroids/name_lc_arr_freq.fits`. The following queries are required.

| Parameter | Type      | Description                             |
| --------- |:---------:|---------:                               |
| name      | str       | name of asteroid in the database.       |
| arr       | str       | ACT array.                              |
| freq      | str       | frequency (GHz) of observation.         |

## Data Output

A valid request to the ACTeroids database will return one of the following:
- `FITS` data file for the request
- an error indicating an invalid request

## References

[Orlowski-Scherer et al. 2023](https://arxiv.org/pdf/2306.05468)

## Change Log

### Version 1.0 (2024 April)

- Initial release

## Citation