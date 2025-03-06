tasks.named<io.quarkus.gradle.tasks.QuarkusBuild>("quarkusBuild") {
    nativeArgs {
        "enabled" to true
        "container-build" to true
        "builder-image" to "quay.io/quarkus/ubi-quarkus-native-image:21.0.0-java11"
    }
}
