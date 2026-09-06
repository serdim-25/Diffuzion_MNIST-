MNIST Generation
Нейронная сеть для генерации новых изображений рукописных цифр.

Результаты

Архитектура: 
UNet(1,28,28) → Begin(1→56) → Down1(56→112) → Down2(112→224) → Bottleneck(224) → Up1(224→112) → Up2(112→56) → Out(56→1) → (1,28,28)

Channels: 1 → 56 → 112 → 224 → 112 → 56 → 1
Spatial:  28 → 28 → 14 → 7 → 14 → 28 → 28

Conditioning: Time (sinusoidal) + Class (one-hot 10)
Skip connections: Down1→Up2, Down2→Up1
