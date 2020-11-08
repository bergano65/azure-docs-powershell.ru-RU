---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075480"
---
# Reset-AzureRoleInstance

## КРАТКИй обзор
Запрос на перезагрузку или переобразировать одиночный экземпляр роли или все экземпляры роли определенной роли.

## Максимальное

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Reset-AzureRoleInstance** запрашивает перезагрузку или переобразировать экземпляр роли, выполняющийся в развертывании.
Эта операция выполняется синхронно.
При перезагрузке экземпляра роли Azure переводит экземпляр в автономный режим, перезапускает основную операционную систему для этого экземпляра и переводит экземпляр обратно в оперативный режим.
Любые данные, которые записываются на локальный диск, сохраняются во всех перезагрузках.
Все данные из памяти будут потеряны.

Reimaging. в зависимости от типа роли, экземпляр роли получает различные действия.
Для веб-или рабочей роли, когда роль воспроизводится, Azure переводит роль в автономный режим и записывает новую установку гостевой операционной системы Azure на виртуальную машину.
Затем роль снова будет переведена в режим онлайн.
При повторном создании роли виртуальной машины Azure переводит ее в автономный режим, повторно применяет к ней настраиваемое изображение и переводит роль обратно в оперативный режим.

Azure пытается поддерживать данные в любых локальных ресурсах хранилища, когда роль передается. Однако в случае временного сбоя оборудования локальный ресурс хранилища может быть потерян.
Если ваше приложение запрашивает сохранение данных, рекомендуется использовать запись в устойчивый источник данных, например на диск Azure.
Любые данные, которые записываются в локальный каталог, отличный от того, который определен локальным ресурсом хранилища, будут потеряны при воссоздании роли.

## ИЛЛЮСТРИРУЮТ

### Пример 1: перезагрузка экземпляра роли
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

Эта команда перезагружает экземпляр роли с именем MyWebRole_IN_0 в промежуточном развертывании службы MySvc01.

### Пример 2: переобразировать экземпляр роли
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

Эта команда переобразует экземпляры ролей в промежуточном развертывании облачной службы MySvc01.

### Пример 3: переизображение всех экземпляров роли
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

Эта команда переобразует все экземпляры роли в рабочем развертывании службы MySvc01.

## ПАРАМЕТРЫ

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

### -InstanceName
Указывает имя экземпляра роли для переустановки или перезагрузки.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Reboot
Указывает, что этот командлет перезагружает указанный экземпляр роли или, если он не указан, для всех экземпляров роли.
Вы должны добавить параметр *reboot* или *Reimage* , но не оба.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Повторное изображение
Указывает на то, что этот командлет переобразировать указанный экземпляр роли или, если он не указан, для всех экземпляров роли.
Вы должны добавить параметр *reboot* или *Reimage* , но не оба.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Указывает имя службы.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Указывает среду развертывания, в которой выполняются экземпляры роли.
Допустимые значения: "производство" и "промежуточный".
Вы можете использовать параметр *DeploymentName* или *slot* , но не оба.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRole](./Set-AzureRole.md)


