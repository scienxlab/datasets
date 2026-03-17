# timeseries

A collection of signals from various sources:

- Matt Hall (2018), Time-frequency decomposition, _The Leading Edge_ **37** (6), p 468–470. DOI: [10.1190/tle37060468.1](https://doi.org/10.1190/tle37060468.1).
- Several recordings are from [`timefreak`](https://github.com/kwinkunks/timefreak), a small collection of signals originally made by various authors at the _Latest developments in time-frequency analysis_ post-convention workshop organized by Mirko van der Baan, Sergey Fomel, and Jean-Baptiste Tary at the SEG Annual Meeting in Denver, Colorado, on 30 October 2014. Read more about this workshop: https://agilescientific.com/blog/2014/11/4/all-the-time-freaks.html.
- The workshop arose from a paper: Tary, J. B., R. H. Herrera, J. Han, and M. van der Baan (2014), Spectral estimation—What is new? What is next?, Rev. Geophys., 52, 723–749, doi:10.1002/2014RG000461. So those signals cite that paper.

The files all contain headers describing the data and specifying the owner and the license.

- **`airgun_800Hz.txt`** &mdash; A marine airgun, used for recording seismic data.
- **`bat_96000Hz.txt`** &mdash; A Vespertilionid bat chirp. 
- **`chiapas_20Hz.txt`** &mdash; A seismic recording of an offshore earthquake in Mexico in 2017.
- **`ecg_500Hz.txt`** &mdash; An electrocardiogram (ECG) record.
- **`irma_1Hz.txt`** &mdash; A seismic recording of Hurricane Irma (2017). 
- **`landslide_100Hz.txt`** &mdash; A seismic recording of a landslide in Greenland in 2017.
- **`laugh_8000Hz.txt`** &mdash; A voice laughing, from Tary et al (2014).
- **`ligo_4096Hz.txt`** &mdash; The gravitational wave from a binary neutron sstart inspiral and collision.
- **`microseismic_2000Hz.txt`** &mdash; A microseismic recording from the Rolla hyraulic frack, from Tary et al (2014).
- **`nuclear_20Hz.txt`** &mdash; A seismic recording of a nuclear test in North Korea in 2017.
- **`piano_22050Hz.txt`** &mdash; A clip from an open recording of Bach's Prelude No. 1 in C major.
- **`seismic_250Hz.txt`** &mdash; A reflection seismic trace.
- **`seismic_synthetic_250Hz.txt`** &mdash; A synthetic seismic trace.
- **`seg_44100Hz.txt`** &mdash; A voice saying, "S E G".
- **`synthetic_250Hz.txt`** &mdash; A toy synthetic signal, from Tary et al (2014).
- **`tohoku_20Hz.txt`** &mdash; A seismic recording of the 2011 earthquake off Japan, from Tary et al (2014).
- **`tremor_100Hz.txt`** &mdash; Mt Redoubt pre-eruption harmonic tremor.
- **`upsweep_400Hz.txt`** &mdash; An [unexplained sound](https://en.wikipedia.org/wiki/List_of_unexplained_sounds) (probably volcanic).

## Read a file with `numpy`

Quick and dirty way to read one of these files:

    import numpy as np
    import matplotlib.pyplot as plt
    
    url = "https://raw.githubusercontent.com/scienxlab/datasets/refs/heads/main/timeseries/synthetic_250Hz.txt"
    
    s = np.loadtxt(url)
    fs = 250  # Hz
    
    dt = 1 / fs
    t1 = s.size * dt
    t = np.arange(0, t1, dt)
    
    fig, ax = plt.subplots(figsize=(15, 2))
    ax.plot(t, s)
