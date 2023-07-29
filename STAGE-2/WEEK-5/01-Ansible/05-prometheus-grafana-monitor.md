## Monitoring
### Monitoring
-  Instal prometheus dan grafan on top docker
-  pull and run promtheus from docker hub
-  ![code26](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/39bbb813-11f4-4ba5-8bba-e26b9570505a)
- ***Note!*** dalam kasus ini saya menjalankan prometheus dengan file volume scrape config
- scrape config prometheus
- ![code28](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/8cd798c4-2ef8-4f10-a84f-13fc03cf6a30)
- ![code27](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/73c7ae37-24fa-4ff1-a1b8-acde273965df)
- Jika sudah berhasil bisa cek dengan ```ip:9090``` untuk prometheus ```ip:9300``` untuk grafana
- ![Screenshot from 2023-07-24 15-02-55](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/f1641984-00e8-4117-85db-1e971ae40cff)
- ![Screenshot from 2023-07-29 23-27-42](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/b001f5b0-d0e0-4fdf-8e10-5cba693aaf38)
- Selajutnya kita akan buat monitoring untuk cpu dan ram untuk appserver
- Tambahkan data source prometheus
- ![Screenshot from 2023-07-24 16-21-38](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/c36567c7-783a-40a9-be4b-ef7c5a52e496)
- ![Screenshot from 2023-07-24 15-26-46](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/041c3dcc-ac82-4ad9-83a3-0d3fbb0cf63e)
- Tambahkan add visualization
- Monitor untuk memory
- ![Screenshot from 2023-07-24 15-25-44](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/9d0a9638-9d60-4dfe-8ebc-bac8182ff599)
- Monitor untuk cpu
- ![Screenshot from 2023-07-24 15-24-22](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/ad9eabae-9c13-43a0-9e3a-72ff5e2cb908)
- ![Screenshot from 2023-07-24 15-26-18](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/dfcaa06e-9edb-488c-a1a1-c3354b62cda9)

### Alerting
- Buat alerting untuk cpu usage overload
- Masuk ke menu alerting
- ![Screenshot from 2023-07-24 16-21-38](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/b8d6fe24-cdf6-4210-9fb5-703361d7648a)
- Buat alert rules
- ![Screenshot from 2023-07-24 15-56-36](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/119fd3d4-b3ae-4f72-ba7e-274a8099152e)
- ![Screenshot from 2023-07-24 16-03-10](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/f6965a0b-b288-4209-a6f0-f59b21836dc6)
- ![Screenshot from 2023-07-24 15-56-41](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/fdbc515a-4c56-4a8d-96fe-5e61309151d5)
- Buat contact point, disini saya menggunakan webhook discord
- ![Screenshot from 2023-07-24 15-50-01](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/ef146a50-d561-4b93-bc3a-30cacd713ffc)
- ![Screenshot from 2023-07-24 16-05-39](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/2d806d37-60ba-44a9-bc2b-2a53e326c5d8)
- ![Screenshot from 2023-07-24 16-05-58](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/d62356d5-06b1-44f1-82ef-7dc24f380761)
