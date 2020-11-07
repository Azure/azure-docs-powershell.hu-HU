---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672401"
---
# Get-AzureRmSiteRecoveryJob

## Áttekintés
Az aktuális webhely-helyreállítási boltozat üzemeltetési adatait kapja meg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByParam (alapértelmezett)
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSiteRecoveryJob** parancsmag Azure webhely-helyreállítási feladatokat kap.
Ezzel a parancsmaggal megtekintheti az aktuális webhely-helyreállítási boltozat üzemeltetési adatait.

## Példák

## PARAMÉTEREK

### -A befejezési időpont
A feladatok befejezési időpontját adja meg.
Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.
Ha egy **datetime** objektumot szeretne beolvasni ehhez a paraméterhez, használja az Get-Date parancsmagot.
További információért írja be a következőt: `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
A webhely-helyreállítási feladatot adja meg.

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
Megadja a feladatot azonosító egyedi nevet.

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

### -Kezdő időpont
A feladatok kezdési időpontját adja meg.
Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State (állami)
A webhely-helyreállítási feladatok beviteli állapotát adja meg.
Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.
A paraméter elfogadható értékei a következők:

- NotStarted
- Előrehaladás
- Sikerességéről
- Más
- Sikertelen
- Lemondott
- Felfüggesztve

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
A feladat által célzott objektum AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 

Required: False
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

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRJob]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Újraindítás – AzureRmSiteRecoveryJob](./Restart-AzureRmSiteRecoveryJob.md)

[Önéletrajz – AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)

[Stop-AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
