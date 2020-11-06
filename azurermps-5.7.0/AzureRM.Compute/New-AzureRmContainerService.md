---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: ff337ae0f5d0da86b035905bf83d2719edf1f4f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492379"
---
# New-AzureRmContainerService

## Áttekintés
Tároló szolgáltatást hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmContainerService** parancsmag létrehoz egy tároló szolgáltatást.
Adja meg a tároló szolgáltatási objektumát, amelyet az New-AzureRmContainerServiceConfig parancsmag használatával hozhat létre.

## Példák

### Példa 1: tároló szolgáltatás létrehozása
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

Az első parancs létrehoz egy ResourceGroup17 nevű erőforráscsoportot a megadott helyen.
További információt az New-AzureRmResourceGroup parancsmag című témakörben találhat.

A második parancs létrehoz egy tárolót, majd a $Container változóban tárolja.
További információt az New-AzureRmContainerServiceConfig parancsmag című témakörben találhat.

A végleges parancs létrehoz egy tároló szolgáltatást a $Containerban tárolt tárolóhoz.
A szolgáltatás neve csResourceGroup17.

## PARAMÉTEREK

### -ContainerService
Az új szolgáltatás tulajdonságait tartalmazó tároló szolgáltatás objektumát adja meg.
**ContainerService** objektum beolvasásához használja az New-AzureRmContainerServiceConfig parancsmagot.

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A parancsmag által létrehozott tároló szolgáltatás nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azt az erőforráscsoport-csoportot adja meg, amelyben a parancsmag telepíti a tároló szolgáltatást.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.

A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmContainerService](./Get-AzureRmContainerService.md)

[Új – AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md)

[Remove-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[Update-AzureRmContainerService](./Update-AzureRmContainerService.md)


