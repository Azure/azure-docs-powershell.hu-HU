---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: 1e637fdad3d6423a5d41eaf4d1dcfe682bf99fd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679855"
---
# New-AzureRmDataFactoryGatewayKey

## Áttekintés
Az Azure Data Factory átjáró kulcsát hozza létre. Ez a parancsmag megszűnt, és Ehelyett használja az **új AzureRmDataFactoryGatewayAuthKey** .

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryName (alapértelmezett)
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmDataFactoryGatewayKey** parancsmag létrehoz egy átjáró kulcsot egy megadott Azure Data Factory átjáróhoz.
Ezzel a kulccsal regisztrálja az átjárót egy Felhőbeli szolgáltatással. Ez a parancsmag megszűnt, és Ehelyett használja az **új AzureRmDataFactoryGatewayAuthKey** .

## Példák

### 1. példa: átjáró-kulcs létrehozása
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

Ez a parancs létrehozza az ContosoGateway nevű adatfeldolgozó-átjáró számára az átjáró kulcsát, majd a pipeline operátor segítségével átadja az átjáró kulcsát az Format-List parancsmagnak.
További információért írja be a következőt: `Get-Help Format-List` .

## PARAMÉTEREK

### -DataFactory
Egy **PSDataFactory** -objektumot ad meg.
Ez a parancsmag létrehoz egy átjáró kulcsot az adatfeldolgozóhoz, amely ezt a paramétert adja meg.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Az adatfeldolgozó nevét adja meg.
Ez a parancsmag létrehoz egy átjáró kulcsot az adatfeldolgozóhoz, amely ezt a paramétert adja meg.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -GatewayName
Az átjáró nevét adja meg.
Ez a parancsmag létrehoz egy kulcsot a paraméter által megadott átjáróhoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy Azure-erőforráscsoport nevét adja meg.
Ez a parancsmag létrehoz egy kulcsot egy olyan átjáróhoz, amely a paraméter által definiált csoportba tartozik.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## KIMENETEK

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayKey

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [Új – AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)


