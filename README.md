tasks.named<io.quarkus.gradle.tasks.QuarkusBuild>("quarkusBuild") {
    nativeArgs {
        "enabled" to true
        // Add other native configurations here if needed
    }
}
plugins {
    kotlin("jvm") version "1.5.31"
    id("io.quarkus") version "2.2.3.Final"
}

dependencies {
    implementation("io.quarkus:quarkus-kotlin")
    implementation("io.quarkus:quarkus-resteasy-reactive")
    // Add other dependencies as needed
}
