---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679020"
---
# Resume-AzureRmSiteRecoveryJob

## Áttekintés
Folytatja a felfüggesztett webhely-helyreállítási feladatot.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByObject (alapértelmezett)
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByName
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **resume-AzureRmSiteRecoveryJob** parancsmag folytatja a felfüggesztett Azure webhely-helyreállítási feladatot.

## Példák

## PARAMÉTEREK

### -Megjegyzések
A Projektnapló megjegyzéseit adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
A webhely-helyreállítási feladat objektumát adja meg.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A feladat egyedi nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### ASRJob
A ' Job ' paraméter elfogadja a "ASRJob" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. SiteRecovery. ASRJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSiteRecoveryJob](./Get-AzureRmSiteRecoveryJob.md)

[Újraindítás – AzureRmSiteRecoveryJob](./Restart-AzureRmSiteRecoveryJob.md)

[Stop-AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
