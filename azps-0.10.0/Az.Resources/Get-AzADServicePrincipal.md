---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 01f6b6d6ed119945af7d99bac9227c788976cbab
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398699"
---
# Get-AzADServicePrincipal

## SYNOPSIS
Szűri az active directory-szolgáltatásban használható egyszerű címtár-rendszereket.

## SZINTAXIS

### EmptyParameterSet (alapértelmezett)
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## LEÍRÁS
Szűri az active directory-szolgáltatásnévben lévő egyszerű címtárat.

## PÉLDÁK

### 1. példa – Az AD szolgáltatásnévsőinek felsorolása

```
PS C:\> Get-AzADServicePrincipal
```

A bérlő összes AD szolgáltatásnévvel rendelkezik.

### 2. példa : Az AD szolgáltatásban használt egyszerű szolgáltatások listájának felsorolása lapozással

```
PS C:\> Get-AzADServicePrincipal -First 100
```

Egy bérlő első 100 AD szolgáltatásának egyszerű felhasználóját sorolja fel.

### 3. példa : Egyszerű szolgáltatásnévlista SPN szerint

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

Az SPN "36f81fc3-b00f-48cd-8218-3879f51ff39f" szolgáltatásnévvel.

### 4. példa : A szolgáltatásnévnév felsorolása keresési karakterlánc alapján

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

Felsorolja azokat az AD szolgáltatásneveket, amelyeknek a megjelenítendő neve "Web" kezdetekkel kezdődik.

### 5. példa : Egyszerű szolgáltatásnév listázása pipázással

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

A (39e64ec6-569b-4030-8e1c-c3c519a05d69) objektumazonosítójú AD alkalmazást, és a Get-AzADServicePrincipal-parancsmagba beömlve felsorolja az adott alkalmazás összes szolgáltatásnévét.

## PARAMETERS

### -ApplicationId
Az egyszerű szolgáltatásalkalmazás azonosítója.

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
Az az alkalmazásobjektum, amelynek a szolgáltatásnév beolvasása folyamatban van.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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
Az egyszerű szolgáltatásnév megjelenítendő neve.

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

### -DisplayNameBeginsWith
Az egyszerű szolgáltatásnév keresési karakterlánca.

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -First
A vissza nem térhet objektumok maximális száma.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Az adatkészletben lévő objektumok számát jelenti. Ez a paraméter jelenleg nem tesz semmit.

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

### -ObjectId
A szolgáltatásnév objektumazonosítója.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
A szolgáltatás SPN-ét.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Figyelmen kívül hagyja az első N objektumot, majd beveszi a fennmaradó objektumokat.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Guid

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Paraméterek: ApplicationObject (ByValue)

## KIMENETEK

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzADServicePrincipal](./New-AzADServicePrincipal.md)


[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADApplication](./Get-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

