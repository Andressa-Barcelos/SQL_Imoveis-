-- MySQL dump 10.13  Distrib 8.0.34, for Win64 (x86_64)
--
-- Host: 127.0.0.1    Database: mydb
-- ------------------------------------------------------
-- Server version	8.0.34

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!50503 SET NAMES utf8 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

--
-- Table structure for table `imoveis`
--

DROP TABLE IF EXISTS `imoveis`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `imoveis` (
  `id` int NOT NULL AUTO_INCREMENT,
  `descricao` varchar(45) NOT NULL,
  `fk_id_tipo_imovel` int NOT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `id_UNIQUE` (`id`),
  KEY `fk_id_tipo_imovel_idx` (`fk_id_tipo_imovel`),
  CONSTRAINT `fk_id_tipo_imovel` FOREIGN KEY (`fk_id_tipo_imovel`) REFERENCES `tipo_imovel` (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=15 DEFAULT CHARSET=utf8mb3;
/*!40101 SET character_set_client = @saved_cs_client */;
--
-- Dumping data for table `imoveis`
--
LOCK TABLES `imoveis` WRITE;
/*!40000 ALTER TABLE `imoveis` DISABLE KEYS */;
INSERT INTO `imoveis` VALUES (1,'Kitnet 50 m²',1),(2,'Apartamento 100 m²',2),(3,'Sobrado 300  m²',3),(4, 'Apartamento 200n m²',4),(5,'Flat 500 m²',5),(6,'Galpao 2500 m²',6),(7,'Sala comercial 250 m²',7), (8,'Apartamento m²',8), (9,'Casa150 m²',9), (10,'Casa 200  m²',10), (11,'Terreno 2000  m²',11),(12,'Apartamento 60 m²',12), (13,'Sobrado 300 m²',13),(14,'Casa 700 m²',14),  (15,'Kitnet 40 m²',15),(16,'Terreno 20000 m²',16),(17,'Flat 1250 m²',17),(18,'Galpao 200 m²',18),(19,'Sobrado 100 m²',19), (20,'Kitnet 60  m²', 20), (21,'Casa 1000 m²', 21), (22,'Sobrado 80 m²', 22),(23,'Apartamento 70 m²', 23),(24,'Galpao 180  m²',24),(25, 'Casa 350 m²', 25),(26, 'Galpao 120 m²', 26),(27, 'Apartamento 68 m²', 27), (28,'Flat 300 m²', 28),(29,'Casa 70 m²', 29),(30,'Flat 120 m²',30);

/*!40000 ALTER TABLE `imoveis` ENABLE KEYS */;
UNLOCK TABLES;
/*!40103 SET TIME_ZONE=@OLD_TIME_ZONE */;

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;

-- Dump completed on 2023-08-31 15:14:35
