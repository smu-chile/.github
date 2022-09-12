# SMU Chile

<div style="text-align: justify;">
SMU nace en diciembre de 2007 a partir de la adquisición de más de 60 cadenas de supermercados, siendo hoy la compañía chilena con mayor cobertura geográfica del país y la única cadena de supermercados presente en las 16 regiones del país. Nuestra estrategia multiformato nos permite satisfacer distintos hábitos de compra entregando las mejores soluciones y productos y el mejor servicio a nuestros clientes.

Contamos con 505 tiendas y 8 centros de distribución en las principales ciudades del país.

Hoy, SMU es el tercer actor de retail supermercadista en Chile. Este gran logro es gracias al trabajo y la dedicación de sus más de 30 mil colaboradores, quienes día a día viven el servicio con entusiasmo y cercanía con el propósito de simplificarle la vida a los clientes.
</div>

## **Internal use**

Los pipeline de **Integración Contínua** están habilitados y documentados en el repositorio [Github Pipelines](https://github.com/smu-chile/gh-reusable-workflows), donde te mostramos como puedes utilizarlos y referenciarlos. De momento los Action permitidos son:

```
PaloAltoNetworks/prisma-cloud-scan@*, SonarSource/sonarcloud-github-action@*, UnicornGlobal/trufflehog-actions-scan@*, actions/checkout@*, actions/download-artifact@*, actions/github-script@*, actions/setup-node@*, actions/upload-artifact@*, amannn/action-semantic-pull-request@*, anchore/sbom-action@*, anchore/scan-action@*, aquasecurity/tfsec-sarif-action@*, aquasecurity/trivy-action@*, bridgecrewio/bridgecrew-action@*, bridgecrewio/checkov-action@*, docker/build-push-action@*, docker/build-push-action@*, docker/login-action@*, docker/metadata-action@*, docker/setup-buildx-action@*, ghe-actions/dockerfile-validator@*, github/codeql-action/analyze@*, github/codeql-action/autobuild@*, github/codeql-action/init@*, github/codeql-action/upload-sarif@*, google-github-actions/auth@v0.8.1, hadolint/hadolint-action@*, hashicorp/setup-terraform@*, hashicorp/setup-terraform@*, haythem/public-ip@*, oke-py/npm-audit-action@*, prisma-cloud-shiftleft/iac-scan-action@v1, smu-chile/aws-ecr-policy-action@*, smu-chile/gh-action-consul-to-env-file@*, smu-chile/gh-action-huawei-swr-policy@*, smu-chile/gh-reusable-workflows/.github/workflows/backend.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/code-security.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/general.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/linter.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/npm-audit.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/npm-registry.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/pkg-build.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/prisma-build-time-front.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/prisma-build-time.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/secure-gh-upload-container-build.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/terraform.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/upload-container-build-time-front.yml@*, smu-chile/gh-reusable-workflows/.github/workflows/upload-container-build-time.yml@*, smu-chile/node-smu/.github/workflows/PrismaCloud.yml@*, smu-chile/node-smu/.github/workflows/action-linter.yml@*, smu-chile/node-smu/.github/workflows/anchore.yml@*, smu-chile/node-smu/.github/workflows/docker-linter.yml@*, smu-chile/node-smu/.github/workflows/docker-sbom.yml@*, smu-chile/node-smu/.github/workflows/snyk.yml@*, smu-chile/node-smu/.github/workflows/trivy.yml@*, smu-chile/node-smu/.github/workflows/trufflehog.yml@*, smu-chile/unit-test-action@*, snyk/actions/docker@*, styfle/cancel-workflow-action@*, trufflesecurity/trufflehog@*
```
Esta lista se irá enriqueciendo y actualizando en la medida que las versiones más recientes cumplan con las necesidades de los distintos equipos. Los miembros de SMU a su vez pueden estar al tanto de los nuevos despliegues de los actions en sus proyectos al implementar un **dependabot.yml** en sus directorios .github para ser notificados en caso de detectar versiones nuevas:

```
version: 2
updates:
- package-ecosystem: "github-actions"
  directory: "/"
  schedule:
    interval: "daily"
```
Este **dependabot.yml** lo puedes encontrar implementado en el repositorio [Github Pipelines](https://github.com/smu-chile/gh-reusable-workflows/tree/master/.github), este levantará un pull request cada vez que encuentre una versión más reciente de los actions utilizados en el proyecto:

<img src="pr-example.png" alt="dependabot PR example" width="500" height="600">

## Templates 🔖
Las plantillas se utilizan para generar nuevos repositorios con una estructura determinada con un solo click, las plantillas que actualmente se encuentran disponibles para los miembros de SMU son:
- [Backend Template](https://github.com/smu-chile/backend-template) Plantilla para el desarrollo de microservicios con arquitectura hexagonal
- [Package Template](https://github.com/smu-chile/pkg-backend-template) Plantilla para la creación de paquetes

## Imagen base 
Se generó una imagen base para la creación de los contenedores de los distintos servicios de SMU 
- [node-smu](https://github.com/smu-chile/node-smu) Imagen base y documentación para su uso.

## Licence

The scripts and documentation in this project are released under the [MIT License](https://github.com/smu-chile/.github/blob/master/LICENSE)
## Contributions

Contributions are welcome! See [Contributor's Guide](https://github.com/smu-chile/.github/blob/master/docs/contributors.md)

## Code of Conduct

👋 Be nice. See our [code of conduct](https://github.com/smu-chile/.github/blob/master/docs/CODE_OF_CONDUCT.md)
