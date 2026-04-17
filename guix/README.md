Guix packages and services for tailscale/tailscaled.

To use this channel, add this to your channels list:

``` scheme
(channel
 (name 'tailscale)
 (url "https://github.com/tailscale/tailscale")
 (branch "main")
 (introduction
 (make-channel-introduction
  "c72e15e84c4a9d199303aa40a81a95939db0cfee"
  (openpgp-fingerprint
   "9E53FC33B8328C745E7B31F70226C10D7877B741"))))
```

After making the change to your channels list, run `guix pull`.

To run tailscale on boot, add `(service tailscale-service-type)` to your `services` list in your Guix configuration.

Everything is in the module `(tailscale tailscale)`.
