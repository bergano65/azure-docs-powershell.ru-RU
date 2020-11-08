---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076382"
---
# Add-AzureProvisioningConfig

## КРАТКИй обзор
Добавляет конфигурацию подготовки для виртуальной машины Azure.

## Максимальное

### Windows (по умолчанию)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureProvisioningConfig** добавляет сведения о конфигурации для подготовки к конфигурации виртуальной машины Azure.
Вы можете использовать объект Configuration для создания виртуальной машины.

Этот командлет поддерживает различные конфигурации подготовки, включая изолированные серверы Windows, серверы Windows, Объединенные с доменом Active Directory и серверами на базе Linux.

Чтобы создать сервер доменных имен Active Directory, укажите полное доменное имя домена Active Directory и учетные данные пользователя, имеющего разрешение на присоединение виртуальной машины к домену.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание автономной виртуальной машины
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

Эта команда создает объект конфигурации виртуальной машины с помощью командлета **New-AzureVMConfig** .
Команда передает этот объект в текущий командлет с помощью оператора конвейера.
Текущий командлет добавляет конфигурацию подготовки для виртуальной машины, работающей под управлением операционной системы Windows.
Конфигурация включает имя пользователя и пароль администратора.
Команда передает конфигурацию в командлет **New-AzureVM** , который создает виртуальную машину.

### Пример 2: создание виртуальной машины, присоединенной к домену
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

Эта команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.
Текущий командлет добавляет конфигурацию подготовки для виртуальной машины, присоединенной к домену contoso.
Команда содержит имя пользователя и пароль, необходимые для присоединения виртуальной машины к домену.
Для настройки требуется, чтобы пользователь изменил пароль пользователя при первом входе.
Команда создает виртуальную машину на основе объекта подготовки.

### Пример 3: создание виртуальной машины на базе Linux
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Эта команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.
Текущий командлет добавляет конфигурацию подготовки для виртуальной машины, работающей под управлением операционной системы Linux.
Конфигурация включает корневое имя пользователя и пароль.
Команда создает виртуальную машину на основе объекта подготовки.

### Пример 4: создание виртуальной машины, включающей сертификаты для WinRM
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Первая команда получает сертификаты из хранилища сертификатов, а затем сохраняет их в переменной массива $certs.

Вторая команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.
Текущий командлет добавляет конфигурацию подготовки, включающую сертификаты для WinRM.
Команда создает виртуальную машину на основе объекта подготовки.

### Пример 5: создание виртуальной машины с поддержкой WinRM по протоколу HTTP
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Эта команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.
Текущий командлет добавляет конфигурацию подготовки с поддержкой WinRM через HTTP.
Команда создает виртуальную машину на основе объекта подготовки.

### Пример 6: создание виртуальной машины с отключенной WinRM по протоколу HTTPS
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Эта команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.
Текущий командлет добавляет конфигурацию подготовки, которая отключает WinRM через HTTPS.
Команда создает виртуальную машину на основе объекта подготовки.

### Пример 7: создание виртуальной машины без экспорта ключа
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Первая команда получает сертификаты из хранилища сертификатов, а затем сохраняет их в переменной массива $certs.

Вторая команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.
Текущий командлет добавляет конфигурацию подготовки для виртуальной машины, включающей сертификаты, и не экспортирует закрытые ключи.
Команда создает виртуальную машину на основе объекта подготовки.

## ПАРАМЕТРЫ

### -AdminUsername
Указывает имя пользователя учетной записи администратора, которую эта конфигурация создает на виртуальной машине.

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Сертификаты
Указывает набор сертификатов, устанавливаемый этой конфигурацией на виртуальной машине.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
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

Если гостевая операционная система — операционная система Windows, эта конфигурация сохранит эти данные как двоичный файл с именем%SYSTEMDRIVE%\AzureData\CustomData.bin.

Если гостевая операционная система — Linux, эти данные передаются с помощью файла ovf-env.xml.
Configuration копирует файл в каталог/var/lib/waagent.
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

### -DisableAutomaticUpdates
Указывает на то, что эта конфигурация отключает автоматические обновления.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Указывает на то, что эта конфигурация отключает инфраструктуру как гостевой агент службы (IaaS).

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

### -DisableSSH
Указывает на то, что эта конфигурация отключает SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Указывает на то, что эта конфигурация отключает удаленное управление Windows (WinRM) на HTTPS.
По умолчанию служба WinRM включена по протоколу HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domain (домен)
Указывает имя домена учетной записи, которая имеет разрешение на добавление компьютера в домен.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
Указывает пароль учетной записи пользователя, у которого есть разрешение на добавление компьютера в домен.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
Указывает имя учетной записи пользователя, у которой есть разрешение на добавление компьютера в домен.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Указывает на то, что эта конфигурация включает WinRM через HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -JoinDomain
Указывает полное доменное имя (FQDN) домена, к которому нужно присоединиться.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Указывает на то, что эта конфигурация создает конфигурацию Linux.

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
Указывает имя пользователя административной учетной записи Linux, которую эта конфигурация создает на виртуальной машине.

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

### -MachineObjectOU
Полное имя подразделения (OU), в котором конфигурация создает учетную запись компьютера.

```yaml
Type: String
Parameter Sets: WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
Эта конфигурация указывает на то, что виртуальная машина создается без конечной точки удаленного рабочего стола.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
Указывает на то, что эта конфигурация создает виртуальную машину без конечной точки SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
Эта конфигурация указывает на то, что виртуальная машина создается без пароля SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Указывает на то, что эта конфигурация не добавляет конечную точку WinRM для виртуальной машины.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
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

### -ResetPasswordOnFirstLogon
Указывает, что виртуальной машине требуется, чтобы пользователь изменил пароль при первом входе.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -Часовой пояс
Указывает часовой пояс для виртуальной машины, например тихоокеанское стандартное время или центральное стандартное время Канады.

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Указывает объект виртуальной машины.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Указывает на то, что эта конфигурация создает автономную виртуальную машину под управлением операционной системы Windows.

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

### -WindowsDomain
Указывает на то, что эта конфигурация создает сервер Windows, который присоединен к домену Active Directory.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Указывает сертификат, который эта конфигурация связывает с конечной точкой WinRM.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
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

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)


