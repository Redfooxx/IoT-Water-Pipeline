# Secure IoT Water Monitoring Pipeline  
An end-to-end security platform developed for a hotel's IoT water monitoring system. The project implements layered defenses—including TLS, mutual TLS, HMAC message signing, replay protection, and AI-powered anomaly detection—to protect critical infrastructure while providing operators with real-time visibility through a live security dashboard.

## Live Demonstration
<video src="https://github.com/user-attachments/assets/0f67abc1-d7fc-4a3f-8cf2-4303e58a523b" width="100%" autoplay loop muted></video>

## Dashboard
<img width="1890" height="905" alt="AI screen shot" src="https://github.com/user-attachments/assets/2eb00a60-e170-44d3-b42e-95be0e2ca8a6" />

## Key Features
- TLS encrypted MQTT communication
- Mutual TLS (mTLS) device authentication
- HMAC message integrity validation
- Timestamp & sequence replay protection
- Isolation Forest anomaly detection
- Real-time security dashboard
- Multi-zone water monitoring
- Live attack simulation

## System Architecture
<img width="469" height="232" alt="image" src="https://github.com/user-attachments/assets/655d4e73-f16c-4638-bbf8-2d6a288c0606" />

## Attack Demonstration

### Eavesdropping
Attempted to intercept MQTT traffic directly from the network.

✅ Blocked by TLS encryption

### Fake Data Injection
Attempted to publish forged sensor readings.

✅ Blocked by mTLS authentication and HMAC validation

### Replay Attack
Attempted to resend previously captured "valid" messages.

✅ Blocked by timestamp freshness and sequence validation

<img width="1740" height="1021" alt="2 Replay Attack Defended" src="https://github.com/user-attachments/assets/135c6991-5c21-45d7-af7a-b1d2626540ef" />

*Replay Attack Defended*

## AI-Powered Detection
Traditional security rules stop malicious messages before they reach the dashboard.

Isolation Forest continuously analyzes sensor behavior to identify abnormal pressure and flow patterns that appear legitimate but differ from normal operating conditions.

Examples include:

- Sudden pressure spikes
- Gradual flow drops
- Sensor drift
- Unusual operating patterns

## Results
✅ 100% replay attacks blocked

✅ Real-time attack detection

✅ TLS overhead of only 0.178%

✅ Multi-zone monitoring dashboard

✅ Live AI anomaly detection

✅ Automatic security event logging
