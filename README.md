# script-install-samba-archlinux
## Procedimentos para execução de Script de instalação/configuração do Samba e de compartilhamento de arquivos no Arch Linux
---

1) Criar o diretório **myscripts** na _home_ executando o seguinte comando:</br>
  `mkdir /home/andre/myscripts`
2) Dentro do diretório _myscripts_ crie com o _Nano_ um arquivo de script com o nome **smbinstall** copiando para dentro dele o conteúdo do arquivo _smbinstall_ disponível neste repositório.</br>

3) Dar permissões de execução ao script antes de executá-lo usando o seguinte comando:</br>
  `sudo chmod +x smbinstall` </br>
4) Alterar o proprietário e o grupo do arquivo **smbinstall** para o do usuário usando os seguintes comandos:</br>
   ```
   sudo chown andre smbinstall
   sudo chown :andre smbinstall
   ```
5) Para que o script seja executável a partir de qualquer local, seguir os procedimentos abaixo:</br>
   -  Editar o arquivo _.bashrc_ usando o comando abaixo:</br>
    `sudo nano .bashrc`

   - Incluir no final do arquivo a seguinte linha:</br>
     `PATH=$PATH:~/myscripts`
    
   - Salvar o arquivo utilizando `CTRL+O` fechar o nano utilizando `CTRL+X`</br>
   
   - Para o comando PATH incluído acima surtir efeito, digite o seguinte comando:</br>
     `source .bashrc`
  
6) Executar o Script que fará a instalação do Samba e as configurações necessárias para compartilhamento de arquivos.
   Para isso utilize o seguinte comando:</br>
   `sudo smbinstall`
7) Após o término da execução do script, reiniciar a máquina

8) Verifique se o samba está instalado e rodando:</br>
``sudo smbstatus``
