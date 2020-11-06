---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: a75eafd57ff7351aa1858114da1cdc7f44b9875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504736"
---
# Get-AzureRmSchedulerJobCollection

## Áttekintés
Begyűjtheti a beosztásokat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSchedulerJobCollection** parancsmag az Azure Scheduler webhelyének munkagyűjteményeit kapja.

## Példák

## PARAMÉTEREK

### -JobCollectionName
A begyűjtő nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azt az erőforráscsoport-csoportot adja meg, amelyből a parancsmag begyűjti a feladatot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. Object (rendszer. objektum)

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disable-AzureRmSchedulerJobCollection](./Disable-AzureRmSchedulerJobCollection.md)

[Enable-AzureRmSchedulerJobCollection](./Enable-AzureRmSchedulerJobCollection.md)

[Új – AzureRmSchedulerJobCollection](./New-AzureRmSchedulerJobCollection.md)

[Remove-AzureRmSchedulerJobCollection](./Remove-AzureRmSchedulerJobCollection.md)

[Set-AzureRmSchedulerJobCollection](./Set-AzureRmSchedulerJobCollection.md)


