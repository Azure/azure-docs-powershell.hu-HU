---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357263"
---
# Get-AzSapMonitor

## SYNOPSIS
Egy SAP-monitor tulajdonságait kapja meg a megadott előfizetéshez, erőforráscsoporthoz és erőforrásnévhez.

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Bej.le
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## LEÍRÁS
Egy SAP-monitor tulajdonságait kapja meg a megadott előfizetéshez, erőforráscsoporthoz és erőforrásnévhez.

## PÉLDÁK

### 1. példa: Az összes SAP-monitor lekérte az előfizetés alatt
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Ez a parancs az SAP-monitorokat egy előfizetés alá kapja.

### 2. példa: SAP-monitor lekért név szerint
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Ez a parancs név szerint SAP-monitort kap.

### 3. példa: SAP-monitor lekérte objektumról objektumra
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Ez a parancs egy SAP-monitort kap objektumról-objektumra.

### 4. példa: SAP-monitor lekérte folyamat szerint
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Ez a parancs egy SAP-monitort kap folyamat alapján.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Az SAP-figyelő erőforrás neve.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.
Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <IHanaOnAzureIdentity> Identity Parameter
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: A törölt tároló helye.
  - `[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve
  - `[ProviderInstanceName <String>]`: A szolgáltatópéldány neve.
  - `[ResourceGroupName <String>]`: Az erőforráscsoport neve.
  - `[ResourceName <String>]`: Az identitáserőforrás neve.
  - `[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.
  - `[Scope <String>]`: Az erőforrás erőforrás-szolgáltatójának hatóköre. Felügyelt identitásokkal bővített szülőerőforrás.
  - `[SubscriptionId <String>]`: Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést. Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.
  - `[VaultName <String>]`: A tároló neve

## KAPCSOLÓDÓ HIVATKOZÁSOK

