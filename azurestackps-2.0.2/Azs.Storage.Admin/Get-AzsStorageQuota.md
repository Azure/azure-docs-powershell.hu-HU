---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016612"
---
# Get-AzsStorageQuota

## Áttekintés


## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Beszerzése
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Leírás


## Példák

### Példa 1:
```powershell
PS C:\> Get-AzsStorageQuota
```

A tárterület-kvóták listájának beszerzése

### 2. példa:
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

A megadott tárolási kvótáról a név alapján tájékozódhat.

## PARAMÉTEREK

### -DefaultProfile


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
A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Hely


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name (név)


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId


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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. models. IStorageAdminIdentity

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IStorageQuota



## MEGJEGYZI

KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.

INPUTOBJECT <IStorageAdminIdentity> : 
  - `[AccountId <String>]`: Belső tárterület-azonosító, amely nem látható a bérlői fiókban.
  - `[AsyncOperationId <String>]`: Aszinkron műveleti azonosító.
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: Erőforrás helye.
  - `[QuotaName <String>]`: A tárolási kvóta neve.
  - `[ResourceGroup <String>]`: Erőforrás-csoport neve.
  - `[ServiceName <String>]`: Storage Service Name (tárterület neve)
  - `[SubscriptionId <String>]`: Előfizetés-azonosító.

## KAPCSOLÓDÓ HIVATKOZÁSOK

