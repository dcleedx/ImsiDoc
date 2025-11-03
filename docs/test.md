이 문서는 윈도우 환경에서 DEEPX M1 모듈을 장착 후에 해당 장치 드라이버를 설치하고 DEEPX 런타임 및 샘플 애플리케이션을 컴파일하여 동작시키는 방법을 제공한다. 



## 시스템 요구사항  
DEEPX M1이 동작하기 위해서는 최소한 다음 시스템 요구사항을 만족해야 한다.

**운영체제:** Windows 10 (64bit) 혹은 Windows 11 (64bit) \
**하드웨어:** M.2 커넥터



## DEEPX M1 윈도우 장치 드라이버 설치

<div class="center-text">
<p align="center">
<img src="./../resources/windows_driver_is_installed.png" alt="DEEPX SDK Architecture" width="650px">  
<br>
Figure. DEEPX SDK Architecture  
<br><br>
</p>
</div>

**DEEPX SDK** is an all-in-one software development platform that streamlines the process of compiling, optimizing, simulating, and deploying AI inference applications on DEEPX NPUs (Neural Processing Units). It provides a complete toolchain, from AI model creation to runtime deployment, optimized for edge and embedded systems, enabling developers to build high-performance AI applications with minimal effort.


Here is the inference flow of **DX-RT**.

<div class="center-text">
<p align="center">
<img src="./../resources/windows_driver_is_not_installed.png" alt="Inference Flow of DXNN Runtime" width="900px">  
<br>
Figure. Inference Flow of DXNN Runtime  
<br><br>
</p>
</div>

This figure illustrates the inference workflow of the DXNN Runtime SDK, which integrates OpenCV-based input/output handling with efficient NPU-accelerated model execution.

**Model Execution**  
The InferenceEngine is the core component of the DXNN Runtime SDK. It:  
- Initializes and controls the NPU device
- Manages memory for input/output tensors
- Schedules inference tasks across NPU and CPU, optimizing their interaction for real-time performance

```
$ cd dx_rt
$ ./install.sh --all
```
---