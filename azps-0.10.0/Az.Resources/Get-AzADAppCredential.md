---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fc8e454328706243e701c0f4df61733562ab73ce
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843482"
---
# Get-AzADAppCredential

## Áttekintés
Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.

## SZINTAXISA

### ApplicationObjectIdParameterSet (alapértelmezett)
```
Get-AzADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az Get-AzADAppCredential parancsmag használatával lekérheti az alkalmazáshoz társított hitelesítő adatok listáját.
Ez a parancs az alkalmazáshoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja kikeresni.

## Példák

### Példa 1 – alkalmazásspecifikus hitelesítő adatok beszerzése objektum-azonosítóval

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

A "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektummal társított hitelesítő adatok listáját számítja ki.

### 2 példa – az alkalmazás hitelesítő adatainak beolvasása csővezetéken

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

Beilleszti az alkalmazást a "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektumazonosítót, és a Get-AzADAppCredential parancsmaghoz illeszti az adott alkalmazás összes hitelesítő adatait.

## PARAMÉTEREK

### -ApplicationId
Az alkalmazás azonosítója a hitelesítő adatok beolvasásához.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
Az Application objektum a hitelesítő adatok beolvasásához.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Az alkalmazás megjelenítendő neve.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
A hitelesítő adatok beolvasására szolgáló alkalmazás objektum-azonosítója.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. GUID

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication
Paraméterek: ApplicationObject (ByValue)

## KIMENETEK

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzADAppCredential](./New-AzADAppCredential.md)

[Remove-AzADAppCredential](./Remove-AzADAppCredential.md)

[Get-AzADApplication](./Get-AzADApplication.md)

