---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075909"
---
# New-AzureQuickVM

## КРАТКИй обзор
Настройка и создание виртуальной машины Azure.

## Максимальное

### Windows (по умолчанию)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureQuickVM** настраивает и создает виртуальную машину Azure.
Этот командлет может развернуть виртуальную машину в существующей службе Azure.
Этот командлет также может создать службу Azure, на которой размещена новая виртуальная машина.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание виртуальной машины
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

Эта команда создает виртуальную машину под управлением операционной системы Windows в существующей службе.
Командлет выдает виртуальную машину на указанном изображении.
Команда задает параметр *WaitForBoot* .
Таким образом, командлет ждет запуска виртуальной машины.

### Пример 2: создание виртуальной машины, использующей сертификаты
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

Первая команда получает сертификаты из хранилища и сохраняет их в переменной $certs.

Вторая команда создает виртуальную машину, которая запускает операционную систему Windows в существующей службе из образа.
По умолчанию на виртуальной машине включен прослушиватель сети WinRM HTTPS.
Команда задает параметр *WaitForBoot* .
Таким образом, командлет ждет запуска виртуальной машины.
Команда отправляет сертификат WinRM и X509Certificates на размещенную службу.

### Пример 3: создание виртуальной машины под управлением операционной системы Linux
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

Эта команда создает виртуальную машину, которая запускает операционную систему Linux из образа.
Эта команда создает службу для размещения новой виртуальной машины.
Команда задает расположение службы.

### Пример 4: создание виртуальной машины и создание службы для размещения новой виртуальной машины
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

Первая команда получает расположения с помощью командлета **Get-AzureLocation** , а затем сохраняет их в переменной массива $Locations.

Вторая команда получает доступные изображения с помощью командлета **Get-AzureVMImage** , а затем сохраняет их в переменной массива $Images.

В последней команде создается большая виртуальная машина с именем VirtualMachine25.
Виртуальная машина запускает операционную систему Windows.
Оно основано на одном из изображений в $Images.
Команда создает службу с именем ContosoService03 для новой виртуальной машины.
Служба находится в папке $Locations.

### Пример 5: создание виртуальной машины с зарезервированным IP-именем
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

Первая команда получает расположения, а затем сохраняет их в переменной массива $Locations.

Вторая команда получает доступные изображения, а затем сохраняет их в переменной массива $Images.

Последняя команда создает виртуальную машину с именем VirtualMachine27 на основе одного из изображений в $Images.
Команда создает службу в месте $Locations.
Виртуальная машина имеет зарезервированное имя IP-адреса, ранее сохраненное в переменной $ipName.

## ПАРАМЕТРЫ

### -AdminUsername
Указывает имя пользователя учетной записи администратора, которую этот командлет создает на виртуальной машине.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AffinityGroup
Указывает территориальную группу для виртуальной машины.
Укажите этот параметр или параметр *Location* только в том случае, если этот командлет создает службу Azure для виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailabilitySetName
Указывает имя группы доступности, в которой этот командлет создает виртуальную машину.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Сертификаты
Указывает список сертификатов, используемых этим командлетом для создания службы.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile
Указывает файл данных для виртуальной машины.
Этот командлет кодирует содержимое файла в формате Base64.
Файл должен быть менее 64 КБ.

Если гостевая операционная система является операционной системой Windows, этот командлет сохраняет эти данные как двоичный файл с именем%SYSTEMDRIVE%\AzureData\CustomData.bin.

Если гостевая операционная система — Linux, этот командлет передает данные с помощью файла ovf-env.xml.
При установке файл копируется в каталог/var/lib/waagent.
Агент также сохраняет данные в кодировке Base64 в/var/lib/waagent/CustomData.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Указывает на то, что этот командлет отключает Гостевой агент "инфраструктура как службу (IaaS)".

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Указывает на то, что этот командлет отключает удаленное управление Windows (WinRM) на HTTPS.
По умолчанию служба WinRM включена по протоколу HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
Указывает массив объектов DNS-серверов, которые определяют параметры DNS для нового развертывания.
Чтобы создать объект **DnsServer** , используйте командлет **New-AzureDns** .

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Указывает на то, что этот командлет включает WinRM через HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Задает режим кэширования узла для диска с операционной системой.
Допустимые значения: 

- Чтения
- Операцию

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
Указывает имя образа диска, используемого этим командлетом для создания диска операционной системы.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Указывает, как этот командлет отвечает на информационное событие.

Для этого параметра допустимы следующие значения:

- Продолжал
- Игнорируйте
- INQUIRE
- SilentlyContinue
- Остановить
- Рвать

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Указывает переменную данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceSize
Задает размер экземпляра.
Допустимые значения: 

- ExtraSmall
- Малого
- Канал
- Достаточ
- ExtraLarge
- Ячейк
- A6
- Ответ
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Указывает на то, что этот командлет создает виртуальную машину на базе Linux.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Указывает имя пользователя административной учетной записи Linux, которое этот командлет создает на виртуальной машине.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Указывает центр обработки данных Azure, на котором размещена виртуальная машина.
Если указать этот параметр, командлет создает службу Azure в указанном расположении.
Указывайте этот параметр или параметр *AffinityGroup* только в том случае, если этот командлет создает службу Azure для виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Указывает место хранения Azure, где этот командлет создает диски виртуальных машин.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя виртуальной машины, созданной этим командлетом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExportPrivateKey
Указывает на то, что эта конфигурация не отправляет закрытый ключ.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Указывает на то, что этот командлет не добавляет конечную точку WinRM для виртуальной машины.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password (пароль)
Указывает пароль учетной записи администратора.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReservedIPName
Задает зарезервированное имя IP-адреса.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReverseDnsFqdn
Указывает полное доменное имя для обратного поиска DNS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Указывает имя новой или существующей службы Azure, к которой этот командлет добавляет новую виртуальную машину.

Если указана новая служба, этот командлет создаст ее.
Чтобы создать новую службу, необходимо указать *Расположение* или параметр *AffinityGroup* .

Если указана существующая служба, не указывайте *Location* или *AffinityGroup*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Задает пары ключей SSH.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Указывает открытые ключи SSH.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetNames
Указывает массив имен подсети для виртуальной машины.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Указывает имя виртуальной сети для виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForBoot
Указывает на то, что этот командлет ожидает, пока виртуальная машина не достигнет состояния ReadyRole.
Если виртуальная машина достигает одного из следующих состояний, командлет завершает работу со сбоем: FailedStartingVM, ProvisioningFailed или ProvisioningTimeout.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Windows
Указывает на то, что этот командлет создает виртуальную машину Windows.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Указывает сертификат, который этот командлет свяжет с конечной точкой WinRM.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Указывает массив сертификатов X509, развернутых в размещенной службе.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureDns](./New-AzureDns.md)


