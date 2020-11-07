---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 7b18a2f5a030a71de0604604b86ba71d2dbe6e03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672455"
---
# Get-AzureRmResource

## Áttekintés

Erőforrásokat kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByTagNameValueParameterSet (alapértelmezett)
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-TagName <String>] [-TagValue <String>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTagObjectParameterSet
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás

A **Get-AzureRmResource** parancsmag Azure-erőforrásokat kap.

## Példák

### Példa 1: a jelenlegi előfizetés összes erőforrásának lekérése

```
PS C:\> Get-AzureRmResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

Ez a parancs a jelenlegi előfizetés összes erőforrását megkapja.

### 2. példa: erőforráscsoport erőforrásainak beolvasása

```
PS C:\> Get-AzureRmResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

Ez a parancs a "testRG" erőforráscsoport összes erőforrását megkapja.

### 3. példa: az összes olyan erőforrás beszerzése, amelynek az erőforráscsoport megegyezik a megadott helyettesítő karakterrel

```
PS C:\> Get-AzureRmResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

Ez a parancs azokat az erőforrásokat kapja meg, amelyek erőforráscsoport az "egyéb" csoportjába tartozik.

### Példa 4: az összes erőforrás beolvasása egy adott névvel

```
PS C:\> Get-AzureRmResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

Ez a parancs minden olyan erőforrást visszanyer, amelynek az erőforrás neve "testVM".

### Példa 5: az összes olyan erőforrás lekérése, akinek a neve megegyezik a megadott helyettesítő karakterrel

```
PS C:\> Get-AzureRmResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

Ez a parancs minden olyan erőforrást beolvas, amelynek az erőforrás neve "teszt"-val kezdődik.

### Példa 6: adott erőforrástípus összes erőforrásának lekérése

```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

Ez a parancs a virtuális gépek jelenlegi előfizetésében található összes erőforrást megkapja.

### 7. példa: erőforrás-erőforrás-azonosító beszerzése

```
PS C:\> Get-AzureRmResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

Ez a parancs az erőforrást a megadott erőforrás-azonosítóval kapja meg, amely a "testRG" erőforráscsoport "testVM" nevű virtuális gép.

## PARAMÉTEREK

### -ApiVersion

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

### -ExpandProperties
Ha meg van adva, kibontja az erőforrás tulajdonságait.

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

### -Name (név)
A beolvasni kívánt erőforrás (ok) neve. Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre

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

### -ResourceGroupName
Az erőforráscsoport a retireved erőforrás (oka) t tartalmazza. Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A teljesen minősített erőforrás AZONOSÍTÓját adja meg, az alábbi példában látható módon. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
A beolvasandó erőforrás (ok) erőforrás-típusa. Példa: Microsoft. számítási/virtualMachines

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címke

A megadott Azure címkét tartalmazó erőforrásokat kapja meg. Írjon be egy, a név vagy a név és az érték kulcsú hash-táblázatot. A helyettesítő karakterek használata nem támogatott. A "címke" egy olyan név-érték páros, amelyet az erőforrásokra és az erőforrás-csoportokra lehet alkalmazni. Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez. Ha hozzá szeretne adni egy címkét egy erőforráshoz, használja az New-AzureRmResource vagy Set-AzureRmResource parancsmagok címke paraméterét. Ha előre definiált címkét szeretne létrehozni, használja az New-AzureRmTag parancsmagot. Ha segítségre van szüksége a Windows PowerShell kivonatoló tábláihoz, futtassa a "Get-Help about_Hashtables" parancsot.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagName
A beolvasni kívánt erőforrás (ok) címkéjének a kulcsa.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagValue
A beolvasandó erőforrás (ok) címke értéke.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. ResourceManagement. models. PSResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Keresés-AzureRmResource](./Find-AzureRmResource.md)

[Move-AzureRmResource](./Move-AzureRmResource.md)

[Új – AzureRmResource](./New-AzureRmResource.md)

[Remove-AzureRmResource](./Remove-AzureRmResource.md)

[Set-AzureRmResource](./Set-AzureRmResource.md)
