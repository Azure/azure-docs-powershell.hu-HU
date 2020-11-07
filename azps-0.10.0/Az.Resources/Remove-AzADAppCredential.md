---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 94a6b1ed2d02e3072a23ccc82fc4a49149b2ae2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843293"
---
# Remove-AzADAppCredential

## Áttekintés
Hitelesítő adatok eltávolítása egy alkalmazásból.

## SZINTAXISA

### ApplicationObjectIdWithKeyIdParameterSet (alapértelmezett)
```
Remove-AzADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdWithKeyIdParameterSet
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationDisplayNameParameterSet
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyIdParameterSet
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A Remove-AzADAppCredential parancsmagot kiegyezéssel vagy a hitelesítő adatok kulcsának lejárati időpontjának részeként lehet eltávolítani egy alkalmazás hitelesítő kulcsával.
Az alkalmazás azonosítása az objektum-azonosító vagy a AppId megadásával történik.
Az eltávolítandó hitelesítő adatok azonosítása a kulcs azonosítója alapján történik.

## Példák

### Példa 1 – meghatározott hitelesítő adatok eltávolítása egy alkalmazásból

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Eltávolítja a "9044423a-60a3-45ac-9ab1-09534157ebb" azonosítójú hitelesítő adatokat a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú alkalmazásból.

### 2. példa – az összes hitelesítő adat eltávolítása egy alkalmazásból

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

A "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" azonosítójú alkalmazásban az összes hitelesítő adat eltávolítása.

### 3 példa – az összes hitelesítő adat eltávolítása a csővezetékekkel

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

Beilleszti az alkalmazást a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú objektumazonosítót, valamint az Remove-AzADAppCredential parancsmaghoz tartozó csöveket, és eltávolítja az adott alkalmazás összes hitelesítő adatait.

## PARAMÉTEREK

### -ApplicationId
Az alkalmazás azonosítója a hitelesítő adatok eltávolításához.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
Az Application objektum a hitelesítő adatok eltávolításához.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
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
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Váltás a hitelesítő adatok törlésére megerősítés nélkül.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
Az eltávolítandó hitelesítőadat-kulcsot adja meg.
Az alkalmazáshoz tartozó kulcs-azonosítók az Get-AzADAppCredential parancsmag használatával szerezhetők be.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Az alkalmazás Object ID-je a hitelesítő adatok eltávolításához.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Ez a beállítás akkor igaz, ha a parancs sikeres.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzADAppCredential](./Get-AzADAppCredential.md)

[Új – AzADAppCredential](./New-AzADAppCredential.md)

[Get-AzADApplication](./Get-AzADApplication.md)
