# calcioKit

A football shirt e-commerce web application built with Java Servlets, JSP and MySQL.

This repository is a fork of [RaffCurcio/calcioKit](https://github.com/RaffCurcio/calcioKit). The original project and its contributors retain their attribution; this README provides an overview of the code available in this fork.

## Features

- Product catalogue, search, filters and product detail pages.
- Registration, login and customer profile management.
- Shopping cart, quantity updates, checkout and order history.
- Administration pages for products and orders.

## Stack

| Layer | Technologies |
| --- | --- |
| Server | Java, Java Servlets, Apache Tomcat |
| Views | JSP, HTML, CSS, JavaScript, jQuery |
| Persistence | MySQL, JDBC, DAO classes |
| Project setup | Eclipse Dynamic Web Project, bundled Gson and MySQL Connector/J |

## Repository structure

```text
calcioKit/
├── db/progetto1.sql          # Database SQL file
└── src/main/
    ├── java/
    │   ├── control/          # Customer-facing servlets
    │   ├── admin/            # Administration servlets
    │   ├── dao/              # Database access
    │   └── model/            # Domain objects
    └── webapp/               # JSP pages, assets and web configuration
```

## Running locally

The checked-in configuration targets **Tomcat 9** and **Servlet 4.0**. It is an Eclipse web project rather than a Maven or Gradle build.

To prepare a local environment, import `calcioKit/` into Eclipse, configure Tomcat and a local MySQL database, review `db/progetto1.sql`, and adapt `src/main/java/dao/DBConnection.java` to your database settings before deployment.

The Java configuration needs alignment: the project facet specifies Java 17, while `.classpath` refers to a JDK 20 installation. Select a consistent local JDK configuration.

These setup notes are based on repository inspection; the application has not been run or tested as part of this documentation update.

## Scope

The checkout implementation records order and payment information in the database. Treat it as demonstration code and use synthetic customer and payment data.
