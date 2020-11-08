---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94088001"
---
# New-AzServiceFabricCluster

## КРАТКИй обзор

Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб. Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете. Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него.

## Максимальное

### ByDefaultArmTemplate (по умолчанию)
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByExistingKeyVault
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNewPfxAndVaultName
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByExistingPfxAndVaultName
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ

В команде **New-AzServiceFabricCluster** используются сертификаты, предоставленные и созданные системой самостоятельно подписанные сертификаты для настройки нового кластера фабрики служб. Используемый шаблон может быть шаблоном по умолчанию или настраиваемым шаблоном, который вы предоставляете. Вы можете указать папку для экспорта самозаверяющих сертификатов или получить их позже из хранилища ключей.
Если вы указываете настраиваемый шаблон и файл параметров, вам не нужно предоставлять информацию о сертификате в файле параметров, система заполнит эти параметры.
Четыре варианта описаны ниже. Прокрутите вниз, чтобы получить объяснения каждого из параметров.

## ИЛЛЮСТРИРУЮТ

### Пример 1: указание только размера кластера, имени субъекта сертификата и операционной системы для развертывания кластера

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

Эта команда задает только размер кластера, имя субъекта сертификата и операционную систему для развертывания кластера.

### Пример 2: Указание существующего ресурса сертификата в хранилище ключей и настраиваемого шаблона для развертывания кластера

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

Эта команда задает существующий ресурс сертификата в хранилище ключей и настраиваемый шаблон для развертывания кластера.

### Пример 3: создание нового кластера с помощью настраиваемого шаблона. Укажите другое имя группы ресурсов для хранилища ключей и добавьте в систему новый сертификат.

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

Эта команда создает новый кластер с помощью настраиваемого шаблона. Укажите другое имя группы ресурсов для хранилища ключей и добавьте в систему новый сертификат.

### Пример 4: создание собственного сертификата и настраиваемого шаблона для создания нового кластера

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

С помощью этой команды вы сможете настроить собственный сертификат и пользовательский шаблон и создать новый кластер.

## ПАРАМЕТРЫ

### -CertificateCommonName

Общее имя сертификата

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFile

Существующий путь к файлу сертификата для основного сертификата кластера

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertificateIssuerThumbprint

Отпечаток поставщика сертификата, отделенный запятыми, если его несколько

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateOutputFolder

Папка нового файла сертификата, который нужно создать.

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertificatePassword

Пароль файла сертификата

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertificateSubjectName

Имя субъекта создаваемого сертификата.

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ClusterSize

Количество узлов в кластере.
По умолчанию — 5 узлов

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile

Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultName

Имя хранилища ключей Azure, если оно не задано, будет использоваться по умолчанию именем группы ресурсов.

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyVaultResourceGroupName

Имя группы ресурсов для хранилища ключей Azure, если оно не задано, будет использоваться по умолчанию именем группы ресурсов.

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location

Расположение группы ресурсов

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)

Укажите имя кластера, если оно не задано, так как оно будет совпадать с именем группы ресурсов.

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OS

Операционная система виртуальных машин, образующих кластер.

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParameterFile

Путь к файлу параметров шаблона.

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName

Укажите имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryCertificateFile

Существующий путь к файлу сертификата для вторичного сертификата кластера

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SecondaryCertificatePassword

Пароль файла сертификата

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SecretIdentifier

Существующий секретный URL-адрес хранилища ключей Azure, например " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TemplateFile

Путь к файлу шаблона.

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Отпечаток
Отпечаток сертификата, correspoinding на SecretIdentifier. Используйте этот параметр, если сертификат не является управляемым, так как в хранилище ключей есть только сертификат, хранящийся в качестве секрета, а командлет не может получить отпечаток.

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VmPassword

Пароль виртуальной машины.

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSku

SKU виртуальной машины

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmUserName

Имя пользователя для входа в VM

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm

Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### System. Security. SecureString

### System. Int32

### Microsoft. Azure. Commands. ServiceFabric. Models. для заданной операционной системе

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
