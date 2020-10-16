# linkbudget
Link Budget Analysis

By definition, link budget is the ratio between the signal powers at the receiver antenna output and the transmitter antenna input. It can be calculated through Friis transmission equation with accounting all the gains and losses across the whole transmitter and receiver chain. Though literally defined by the effective transmission and reception signal powers, it highly depends on the channel betwwen the transitter and receiver pair, which is a function of bandwidth, multipath and attenuation in general.

## Signal Processing Perspecives
From a Friis equation and a signal processing perspective, link budget (in dBm) improves logarithmically with increasing signal spreading gain and reducing signal bandwidth, in addition to transmitted signal power. The catch, however, is as you increase the signal spreading gain or coding gain in time domain or reduce the signal bandwidth in frequency domain, the device's battery life itself is reduced, accordingly.  In other words, if you want to improve the cell coverage of a IoT system,  then the battery life of served IoT devices will be shortened, except to use a larger battery.


## Information Theory Perspectives
When the limits and bottomlines between the link budget and battery life tradeoffs are concerns, information theory traditionally is the theory framework and tool for under standing the patterns underneath. From an information theory standing-point, the minimum energy per bit to noise power spectral density ratio Eb/No = Es/r/N0 is determined by Shannon equation with L'Hôpital rule to be greater than ln(2) = -1.59 dB, whatever the coding and modulation schemes are used.  This means, for a reliable transmission, including making a connection through RACH procedure or sending an ACK or NAK, between a transmitter and a receiver, the received signal energy per bit shall be greater than the Shannon minimum energy requirement, which is 1.59 dB below the noise floor. Accordingly if we consider a IoT system with a bandwidth of 1 kHz, a spreading gain of 64, a 4-antenna receiver and 10 dB co-channel interference, the Shannon maximum link budge is about 177 dB.
