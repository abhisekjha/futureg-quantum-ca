# SIMLESS: Post-Quantum EAP-TLS Architecture for Scalable IoT in Next-Generation Networks

Next-generation (FutureG) networks will interconnect billions of IoT devices, demanding scalability, reliability, and robust security against quantum threats. Conventional SIM-based protocols (e.g., EAP-AKA) are unsuitable for massive IoT due to complex provisioning and limited post-quantum readiness. This paper introduces a post-quantum EAP-TLS framework integrating Kyber and Dilithium cipher suites, edge-assisted computation, and decentralized certificate management to offload heavy cryptographic tasks from constrained devices. Experimental results show a 96.49\% reduction in handshake time, a 2033.13\% throughput improvement when offloading cryptographic operations to the edge, and efficient session resumption for reduced latency. These findings demonstrate that breaking the SIM barrier and leveraging edge-assisted PQC significantly enhances scalability and security, paving the way for unified, quantum-safe authentication in FutureG networks.


![FutureG Network](images/no_of_experiments.png)
![ost-Quantum Safe Simless TLS Architecture](simless.png)

## Steps to Run the Test

1. **Activate the environment**
   ```bash
   source venv/bin/activate
   ```

2. Git clone the `pqc_aes_multipath` repo:
```bash
https://github.com/abhisekjha/NextGenSecureMessaging.git
cd pqc_aes_multipath
```

3. git clone `Kyber based PYKY`
```bash
https://github.com/asdfjkl/pyky.git
```

4. git clone `Dilithium` and rename it to `dilithium`
```bash
https://github.com/GiacomoPope/dilithium-py
```


5. Set and verify Pythonpath:
``` sh
export PYTHONPATH=/path/to/NextGenSecureMessaging:/path/to/NextGenSecureMessaging/pyky:/path/to/NextGenSecureMessaging/dilithium
echo $PYTHONPATH
```

6. Install requirements.txt
```
pip install -r requirements.txt
```
7. Run test cases using make
```
make
```

## Acknowledgements

I would like to thank the [pyky](https://github.com/asdfjkl/pyky) repository and [dilithium-py](https://github.com/GiacomoPope/dilithium-py) for providing the implementation of the Kyber cryptographic algorithm and Dilithium Implementation, which was used in this project.
