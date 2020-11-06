---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 616b75b4bdc5dab9f02bb1fc295effefc0e728be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491857"
---
# New-AzureRmPolicyAssignment

## Áttekintés
Házirend-hozzárendelést hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### DefaultParameterSet (alapértelmezett)
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### PolicyParameterObjectParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicyParameterStringParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicySetParameterObjectParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicySetParameterStringParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmPolicyAssignment** parancsmag létrehoz egy házirend-feladatot.
Adjon meg egy házirendet és egy hatókört.

## Példák

### 1. példa: házirend-hozzárendelés az erőforrás csoport szintjén
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzureRMResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.
A második parancs a VirtualMachinePolicy nevű házirend-definíciót a Get-AzureRmPolicyDefinition parancsmag használatával kapja meg, és a $Policy változóban tárolja.
A végleges parancs a házirendet a $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport szintjén rendeli $Policy.

### 2. példa: házirend-hozzárendelés az erőforráscsoport szintjén a házirend-paraméter objektummal
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.
A parancs az objektumot a $ResourceGroup változóban tárolja.
A második parancs az engedélyezett helyek beépített házirend-definícióját az Get-AzureRmPolicyDefinition parancsmag használatával kapja meg.
A parancs az objektumot a $Policy változóban tárolja.
A harmadik és a negyedik parancs a nevében a "Kelet" nevű összes Azure-régiót tartalmazó objektumot hoz létre.
A parancsok az objektumot a $AllowedLocations változóban tárolják.
A végleges parancs az $AllowedLocationsban a Policy paraméter objektummal az erőforráscsoport szintjén rendeli hozzá a házirendet a $Policyban.
A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.

### 3. példa: házirend-hozzárendelés az erőforráscsoport szintjén a házirend-paraméter fájllal
A következő tartalommal hozzon létre egy _AllowedLocations.js_ nevű fájlt a helyi munkakönyvtárban.

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzureRMResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.
A második parancs beolvassa az engedélyezett helyek beépített házirend-definícióját az Get-AzureRmPolicyDefinition parancsmag használatával, és a $Policy változóban tárolja.
A végleges parancs kiosztja a házirendet $Policy a $ResourceGroup **ResourceId** tulajdonság által meghatározott erőforráscsoport AllowedLocations.jsa helyi munkakönyvtárban a Policy paramétert tartalmazó fájllal.

### 4. példa: házirend-hozzárendelés felügyelt identitással
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot az Get-AzureRMResourceGroup parancsmag használatával, és a $ResourceGroup változóban tárolja.
A második parancs a VirtualMachinePolicy nevű házirend-definíciót a Get-AzureRmPolicyDefinition parancsmag használatával kapja meg, és a $Policy változóban tárolja.
A végleges parancs a házirendet a $Policy az erőforráscsoport-csoportba rendeli. A rendszer automatikusan létrehoz egy felügyelt identitást, és hozzárendeli a házirend-hozzárendeléshez.

## PARAMÉTEREK

### -ApiVersion
Az erőforrás-szolgáltató API-nak a verziószámát adja meg.
Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.

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

### -AssignIdentity
Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez Az identitás a "deployIfNotExists" házirendek telepítésének végrehajtásakor lesz használatos. Az identitás hozzárendelésekor a hely szükséges.

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

### -Leírás
A házirend-hozzárendelés leírása

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
A házirend-hozzárendelés megjelenítendő nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.
A paraméter elfogadható értékei a következők:
- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A házirend-hozzárendelés erőforrás-identitásának helye. Erre akkor van szükség, ha a-AssignIdentity kapcsolót használja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Metadata
Az új házirend-hozzárendelés metaadatai. Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A házirend-hozzárendelés nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotScope
A házirend-hozzárendeléshez nem tartozó hatókörök

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinition
A házirendet adja meg **PsPolicyDefinition** -objektumként, amely a házirend-szabályt tartalmazza.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameter
A házirend paraméterének fájlelérési útja vagy a házirend paraméterének karakterlánca.

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameterObject
A Policy paraméter objektuma.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicySetDefinition
A Policy set definition objektum.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.

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

### -Scope (hatókör)
A házirend hozzárendelésének hatókörét adja meg.
Ha például egy erőforrás-csoporthoz szeretne házirendet rendelni, adja meg a következőt: `/subscriptions/` előfizetés azonosítója `/resourcegroups/` Erőforrás-csoport neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
A SKU tulajdonságokat reprezentáló kivonatoló táblázat. Az alapértelmezett érték a szabad SKU értékkel az értékekkel: `@{Name = 'A0'; Tier = 'Free'}` . A standard SKU használatához használja az értékeket: `@{Name = 'A1'; Tier = 'Standard'}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmPolicyDefinition](./Get-AzureRmPolicyDefinition.md)

[Get-AzureRmPolicyAssignment](./Get-AzureRmPolicyAssignment.md)

[Remove-AzureRmPolicyAssignment](./Remove-AzureRmPolicyAssignment.md)

[Set-AzureRmPolicyAssignment](./Set-AzureRmPolicyAssignment.md)


