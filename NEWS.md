## Harminv 1.3.1

* Fixed the phase output column to have the same sign as the documentation
  (the sign was flipped).  Thanks to Andrew Norton for the bug report.

* Added `-n` option to flip the sign of the frequency convention.

## Harminv 1.3:

* Switch back to eigensolver technique used in Harminv 1.0.x, which first
  removes the singular null space as described by Wall and Neuhauser.
  This seems to make the solution much more stable and reliable.  The
  command-line tool once again defaults to 100 basis modes rather than
  a particular spectral density.

## Harminv 1.2.1:

* Impose a maximum number of basis modes (300) to prevent the matrices
  from getting too large.

* Corrected typo in man page (for definition of `-d` density).

## Harminv 1.2:

* Command line tool now defaults to a particular spectral "density"
  (set by the `-d` option), rather than a number of basis modes,
  since using too many basis modes leads to a singular eigenproblem
  and numerical instability.  (Based on defaults from M&T references.)

* Use `long double` precision, if available, to reduce accumulation
  of floating-point errors while computing Fourier/Z transforms.

## Harminv 1.1:

* Corrected bug in frequency-error calculation; thanks to V. A.
  Mandelshtam for helpful discussions and for letting me look
  at his code to check against mine.

* Amplitude calculation is no longer unstable for strongly decaying modes.

* Used a more accurate eigensolver routine.

* Added `-e`/`-E`/`-a`/`-A`/`-Q` options to screen outputs with
  error/amplitude/Q too large/small/small, respectively.

* Added `-w` option to use angular frequency instead of frequency.

* More flexible input format: allow comma-delimited, a-bi as well as a+bi.

* API cleanups.

## Harminv 1.0.2:

* Corrected inadvertent windowing of data that degraded accuracy
  in the case of very short signals.

## Harminv 1.0.1:

* Corrected some minor release glitches.

## Harminv 1.0:

* Initial release (after 4 years of private use).