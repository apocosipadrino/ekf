# EKF · 2D Localization — Interactive Visualization

An interactive, self-contained simulation of an Extended Kalman Filter
localizing a robot driving in a circle, using range-and-bearing measurements
to four known landmarks. No dependencies: open `index.html` in a browser
(or serve it with GitHub Pages).

What it shows:

- **Predict step:** the motion model moves the estimate and the 95%
  covariance ellipse grows.
- **Update step:** range/bearing measurements correct the estimate through
  the Kalman gain, and the ellipse shrinks.
- **Dead reckoning alone** (gray trail) drifts without bound. The EKF stays
  close to the true pose thanks to the measurements.

Controls: Auto / Predict / Update / Reset, plus sliders for process noise (Q)
and measurement noise (R). The filter linearizes the nonlinear motion and
measurement models with Jacobians around the current estimate — that is the
"extended" in EKF.
