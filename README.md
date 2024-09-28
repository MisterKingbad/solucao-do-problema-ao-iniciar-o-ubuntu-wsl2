# Solução do problema ao iniciar o ubuntu wsl2

## Um exemplo de erro ao iniciar o ubuntu WSL2
```bash
Habilite o recurso Plataforma de Máquina Virtual do Windows e verifique se a virtualização está habilitada no BIOS.     Para obter mais informações, acesse https://aka.ms/wsl2-install                                                         Press any key to continue...    
```
## Comandos
```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
```bash
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
Reinicie o pc e depois execute
```bash
DISM /Online /Enable-Feature /All /FeatureName:Microsoft-Hyper-V
```
```bash
bcdedit /set hypervisorlaunchtype auto
```
Reinicie o pc e depois pronto.
