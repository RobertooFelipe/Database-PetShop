-- phpMyAdmin SQL Dump
-- version 4.9.5
-- https://www.phpmyadmin.net/
--
-- Host: localhost
-- Tempo de geração: 17/11/2020 às 21:56
-- Versão do servidor: 10.3.25-MariaDB-log
-- Versão do PHP: 7.4.11

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Banco de dados: `jrconsul_anch_g2`
--

-- --------------------------------------------------------

--
-- Estrutura para tabela `Acessorios`
--

CREATE TABLE `Acessorios` (
  `CODIGO` int(20) NOT NULL,
  `PRECO` float NOT NULL,
  `NOME` varchar(100) NOT NULL,
  `QNTD` int(10) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Estrutura para tabela `cadastro_cliente`
--

CREATE TABLE `cadastro_cliente` (
  `CPF` varchar(40) NOT NULL,
  `ENDERECO` varchar(40) NOT NULL,
  `NOME` varchar(40) NOT NULL,
  `TEL` varchar(40) NOT NULL,
  `NOME_ANIMAL` varchar(20) NOT NULL,
  `ANIMAL` varchar(20) NOT NULL,
  `RACA` varchar(20) NOT NULL,
  `IDADE` int(20) NOT NULL,
  `OUTROS` varchar(100) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Despejando dados para a tabela `cadastro_cliente`
--

INSERT INTO `cadastro_cliente` (`CPF`, `ENDERECO`, `NOME`, `TEL`, `NOME_ANIMAL`, `ANIMAL`, `RACA`, `IDADE`, `OUTROS`) VALUES
('14725836955', 'Teste Teste 147', 'Teste', '11942953291', 'TesteTeste', 'Teste', 'Teste', 11, 'TesteTesteTesteTesteTeste');

-- --------------------------------------------------------

--
-- Estrutura para tabela `Estoque`
--

CREATE TABLE `Estoque` (
  `CODIGO` int(20) NOT NULL,
  `PRECO` float NOT NULL,
  `NOME` varchar(100) NOT NULL,
  `QNTD` int(10) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Estrutura para tabela `Saude`
--

CREATE TABLE `Saude` (
  `CODIGO` int(20) NOT NULL,
  `PRECO` float NOT NULL,
  `NOME` varchar(100) NOT NULL,
  `QNTD` int(10) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Índices de tabelas apagadas
--

--
-- Índices de tabela `Acessorios`
--
ALTER TABLE `Acessorios`
  ADD PRIMARY KEY (`CODIGO`);

--
-- Índices de tabela `cadastro_cliente`
--
ALTER TABLE `cadastro_cliente`
  ADD PRIMARY KEY (`CPF`);

--
-- Índices de tabela `Estoque`
--
ALTER TABLE `Estoque`
  ADD PRIMARY KEY (`CODIGO`);

--
-- Índices de tabela `Saude`
--
ALTER TABLE `Saude`
  ADD PRIMARY KEY (`CODIGO`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
