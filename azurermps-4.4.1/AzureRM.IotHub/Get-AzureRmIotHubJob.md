---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: b0ea6f3cae3fe978a3d24b055eb47693ea466272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679436"
---
# Get-AzureRmIotHubJob

## Áttekintés
Információt kap egy IotHub-feladatról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Információt kap egy IotHub-feladatról.
Az IotHub-feladat akkor jön létre, ha az importálási vagy exportálási műveletet az New-AzureRmIotHubExportDevices vagy a New-AzureRmIotHubImportDevices parancs segítségével hozza létre.
A projekt azonosítóval listázhatja az összes feladatot, vagy szűrheti a feladatokat.

## Példák

### Példa 1 minden feladat listázása
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

A "myiothub" nevű IotHub minden feladatát kapja

### Példa 2 adott feladat beszerzése
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

Információt kap a feladatról a "3630fc31-4caa-43e8-A232-ea0577221cb2" azonosítóval az "myiothub" nevű IotHub.

## PARAMÉTEREK

### -JobId
A projekt azonosítója. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A IoT-központ neve. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név

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

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse
System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Command. Management. IotHub. models. PSIotHubJobResponse, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null\]\]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

