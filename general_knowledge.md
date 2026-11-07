# knowledge

## backoff

Backoff is a strategy used in computing to handle failed operations by waiting longer between each retry, preventing system overload. It improves resilience in distributed systems by addressing transient errors or high load. It is often used with "jitter" (randomized delays) to distribute, not just delay, traffic spikes.

Exponential Backoff: A method where the wait time between retries increases exponentially, for example: 1s, 2s, 4s, 8s....
