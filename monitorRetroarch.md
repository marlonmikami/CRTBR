# Conseguindo 240p verdadeiros com o retroarch

### Configurando as resoluções necessárias

[CRU](https://custom-resolution-utility.en.lo4d.com/windows) permite que você crie resoluções personalizadas. Usaremos essa aplicação para criar uma resolução de 1920x240, 120Hz.

Coloque os valores da imagem no CRU, rode o executável restart64.exe e pronto.

![cru](images/cru.jpeg)

### Configurando o retroarch

Agora precisamos configurar o retroarch para usar a resolução que acabamos de criar. Você pode pegar o retroarch.cfg deste repositório, ou apenas editar os campos a seguir:

```
video_fullscreen = "true"
video_windowed_fullscreen = "false"
video_fullscreen_x = "1920"
video_fullscreen_y = "240"
aspect_ratio_index = "22"
video_refresh_rate = "120.000000"
crt_switch_resolution = "3"
crt_switch_resolution_super = "1920"
menu_driver = "rgui"
```

Tenha em mente que essas configurações podem ser salvas como core overrides, case queira usar uma resolução maior para o menu principal do retroarch.

Segue os meus resultados:

![consoles](images/consoles.jpg)

# Wii & PS2
O Wii e o PS2 podem ser conectados nomonitor CRT usndo um conversor de Componente para VGA. O que eu tenho me permite mudar a resolução (começando em 480p) e a proporção da imagem, além de outros ajustes de imagem.

Esse tipo de conversor pode ser encontrado no [Aliexpress](https://pt.aliexpress.com/item/1005002393774648.html?spm=a2g0o.detail.1000060.1.cc6a72a4Lg4Y9k&gps-id=pcDetailBottomMoreThisSeller&scm=1007.13339.291025.0&scm_id=1007.13339.291025.0&scm-url=1007.13339.291025.0&pvid=8be36fc2-dae1-4634-a140-6ffe1f39f0dd&_t=gps-id%3ApcDetailBottomMoreThisSeller%2Cscm-url%3A1007.13339.291025.0%2Cpvid%3A8be36fc2-dae1-4634-a140-6ffe1f39f0dd%2Ctpp_buckets%3A668%232846%238116%232002&pdp_ext_f=%7B%22sku_id%22%3A%2212000020523449551%22%2C%22sceneId%22%3A%223339%22%7D&pdp_npi=2%40dis%21BRL%21430.93%21258.55%21%21%21%21%21%402101f6b116747343014295494ed6a9%2112000020523449551%21rec&gatewayAdapt=glo2bra) (Não estou recomendando esse vendedor em particular, este é apenas o primeiro conversor que eu encontrei que parece igual ao que eu tenho)

![ps2wii](images/ps2wii.jpg)

![ypbpr2vga](images/ypbpr2vga.jpg)

# Nintendo 64

Eu estou trabalhando em conectar o Nintendo 64 no monitor CRT (os emuladores de N64 são péssimos, então prefiro usar o hardware original). Testes com um conversor barato de composto para VGA me deram uma imagem bem feia, então estou procurando alternativas.
