---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493378"
---
# Get-AzureRmADSpCredential

## Áttekintés
Lekérdezi a szolgáltatóhoz társított hitelesítő adatok listáját.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ObjectIdParameterSet (alapértelmezett)
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A Get-AzureRmADSpCredential parancsmag használatával lekérdezheti a szolgáltatóhoz társított hitelesítő adatok listáját.
Ez a parancs a szolgáltatóhoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja visszakeresni.

## Példák

### --------------------------Példa 1--------------------------
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

Az SPN-t tartalmazó szolgáltatóhoz társított hitelesítő adatok listáját számítja ki http://test12345 .

## PARAMÉTEREK

### -ObjectId
A szolgáltatás megbízójának objektum azonosítója a hitelesítő adatok beolvasásához.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
A szolgáltatás megbízójának neve (SPN) a hitelesítő adatok beolvasásához.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
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

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Remove-AzureRmADSpCredential](./Remove-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

