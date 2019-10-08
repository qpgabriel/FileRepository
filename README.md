### Requirements
- MYSQL Connector 5.1.47
- Apache Tomcat v8.5
## BD name: webcamadas

-- Table structure for table `arquivo`

CREATE TABLE `arquivo` (
  `id` int(11) NOT NULL,
  `id` int(11) NOT NULL,
  `titulo` varchar(30) COLLATE utf8_bin NOT NULL,
  `conteudoTipo` varchar(20) COLLATE utf8_bin NOT NULL,
  `autor` varchar(30) COLLATE utf8_bin NOT NULL,
  `dataCriacao` date NOT NULL,
  `arquivo` blob NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin;

-- Table structure for table `user`

CREATE TABLE `user` (
  `username` varchar(30) COLLATE utf8_bin NOT NULL,
  `password` varchar(20) COLLATE utf8_bin NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_bin;

-- Indexes for table `arquivo`

ALTER TABLE `arquivo`
  ADD PRIMARY KEY (`id`);
  ADD FOREIGN KEY (`username`)
        REFERENCES username (`user`)

-- Indexes for table `user`

ALTER TABLE `user`
  ADD PRIMARY KEY (`username`);

-- AUTO_INCREMENT for table `arquivo`

ALTER TABLE `arquivo`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;
