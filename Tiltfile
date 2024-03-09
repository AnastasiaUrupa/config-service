# Build
custom_build(
  # Name of the container image
  ref = 'config-service',
  # Command to build the container image
  command = './gradlew bootBuildImage --imageName $EXPECTED_REF',
  # Files to watch that trigger a new build
  deps = ['k8s']
)

# Deploy
k8s_yaml(['k8s/deployment.yml', 'k8s/service.yml'])