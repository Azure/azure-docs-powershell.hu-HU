---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672690"
---
# Install-AzureRmServerManagementGatewayProfile

## Áttekintés
Kiszolgálói felügyeleti átjáró-profil telepítése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **telepítés-AzureRmServerManagementGatewayProfile** parancsmag a megfelelő helyre telepíti az Azure Server Management Gateway-profilt.
A parancsmag által telepített fájl neve profile.js.

## Példák

## PARAMÉTEREK

### -InputFile
Annak a helyi fájlnak a neve, amely a telepítendő átjáró profilt tartalmazza.

A parancsmag által telepített fájlt előzőleg az Save-AzureRmServerManagementGatewayProfile parancsmaggal kellett menteni.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### FileInfo
A ' InputFile ' paraméter az "FileInfo" típusú értéket fogadja el a csővezetékről

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Reset-AzureRmServerManagementGatewayProfile](./Reset-AzureRmServerManagementGatewayProfile.md)

[Mentés-AzureRmServerManagementGatewayProfile](./Save-AzureRmServerManagementGatewayProfile.md)


