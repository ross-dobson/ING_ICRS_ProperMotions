# ING_ICRS_ProperMotions
Convert ICRS milliarcsecond/year proper motions to the INT format: $\mu_\alpha$ in sec/year and $\mu_\delta$ in arcsec/year.

ICRS proper motions for both Right Ascension and Declination, $\mu_\alpha$ and $\mu_\delta$ respectively, are generally quoted in units of milliarcseconds (mas) per year. However the [ING TCS catalogue format](https://www.ing.iac.es/Astronomy/telescopes/wht/catformat.html) used on the Isaac Newton Telescope and William Herschel Telescopes requires $\\mu_\\alpha$ in seconds per year (i.e. seconds of "time"/right ascension, not arcseconds of a degree!), and $\mu_\delta$ in arcseconds per year.

For $\mu_\delta$, that's an easy enough conversion - just multiply by 1000. For the proper motion in right ascension though, the calculation is less straightforward, as we need to convert from arcseconds of degree to seconds of right ascension, using $15^" \times \cos(\delta)$, where $\delta$ is the declination of the target in degrees.

**N.B. This is for proper motion of targets that will still be sidereally tracked. This is _not_ for differential/non-sidereal tracking (e.g. asteroids), which are in second/second and arcsecond/second respectively. See [the TCS manual](https://www.ing.iac.es/~docs/int/tcs/int-tcs-1/int-tcs-1.pdf) for more information.**
