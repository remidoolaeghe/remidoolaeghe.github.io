---
layout: post
title: Comment changer la version Java utilisée par Maven sur Mac OS X
subtitle: Ou comment passer sous Java 8
category: lesmainsdanslecambouis
tags: maven java OSX
feature-image: 2015-06-17-Configurer_la_version_java_de_Maven-feature-image.png
---

Je vous propose une traduction de cet [article](http://blog.tompawlak.org/maven-default-java-version-mac-osx) de *Tom Pawlak* qui m'a permis de passer un de mes projets sous Java 8 sur **Mac OS X**. J'étais capable de lancer un build **Maven** depuis mon **IDE** préféré, mais pas depuis la ligne de commande dans mon **shell** favori. L'article parle de passer sous **Java 7**, mais la manipulation est la même à un chiffre près. Je vous laisse deviner lequel.

# Traduction

Récemment, j'ai installé [Maven 3.2.1](https://maven.apache.org/docs/3.2.1/release-notes.html) sur **Mac OS X**, et j'ai découvert que **Maven** n'utilisait pas ma version par défaut de **Java** (définie comme étant la **1.7**). Au lieu de ça, il utilisait la version **1.6**.

La commande `java -version` donnait le résultat suivant :

{% highlight console %}
java version "1.7.0_51"
Java(TM) SE Runtime Environment (build 1.7.0_51-b13)
Java HotSpot(TM) 64-Bit Server VM (build 24.51-b03, mixed mode)
{% endhighlight %}

L'équivalent **Maven**, à savoir `mvn --version`, donnait le résultat suivant :

{% highlight console %}
Apache Maven 3.2.1 (ea8b2b07643dbb1b84b6d16e1f08391b666bc1e9; 2014-02-14T17:37:52+00:00)
Maven home: /usr/local/apache-maven-3.2.1
Java version: 1.6.0_65, vendor: Apple Inc.
Java home: /System/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home
Default locale: en_US, platform encoding: MacRoman
OS name: "mac os x", version: "10.9.3", arch: "x86_64", family: "mac"
{% endhighlight %}

Après un rapide coup d'oeil à la commande de lancement de **Maven** (`$M2_HOME/bin/mvn`) , vous pourrez constater que **Maven** lit au démarrage les deux fichiers `/etc/mavenrc` et `~/.mavenrc`. Tout ce que j'avais à faire était de créer un de ces deux fichiers (j'ai choisi `/etc/mavenrc` pour appliquer la configuration à tous les utilisateurs du système) et assigner le chemin du **home** de **Java 1.7** à la variable d'environnement `JAVA_HOME`.

**Mac OS X** dispose de la commande `/usr/libexec/java_home` qui retourne un chemin utilisable pour configurer la variable d'environnement **JAVA_HOME**.

Au final, mon fichier contenait la ligne suivante :

{% highlight console %}
JAVA_HOME=`/usr/libexec/java_home`
{% endhighlight %}

Après ce changement, **Maven** utilise la bonne version de **Java**. La commande `mvn --version` indique désormais :

{% highlight console %}
Apache Maven 3.2.1 (ea8b2b07643dbb1b84b6d16e1f08391b666bc1e9; 2014-02-14T17:37:52+00:00)
Maven home: /usr/local/apache-maven-3.2.1
Java version: 1.7.0_51, vendor: Oracle Corporation
Java home: /Library/Java/JavaVirtualMachines/jdk1.7.0_51.jdk/Contents/Home/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "mac os x", version: "10.9.3", arch: "x86_64", family: "mac"
{% endhighlight %}

# Bibliographie

 [L'article original de *Tom Pawlak*](http://blog.tompawlak.org/maven-default-java-version-mac-osx)

[La release note de Maven 3.2.1](https://maven.apache.org/docs/3.2.1/release-notes.html) 

[La commande java_home de Mac OSX](https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man1/java_home.1.html)