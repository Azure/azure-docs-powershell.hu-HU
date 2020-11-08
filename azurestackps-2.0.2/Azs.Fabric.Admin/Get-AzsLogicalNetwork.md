---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalnetwork
schema: 2.0.0
ms.openlocfilehash: 8229e487cd7c616969e049bbbea0ba7a6a18a448
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016663"
---
# Get-AzsLogicalNetwork

## Áttekintés
A kért logikai hálózat értékét számítja ki.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsLogicalNetwork -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsLogicalNetwork -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Leírás
A kért logikai hálózat értékét számítja ki.

## Példák

### Példa 1:
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

Minden logikai hálózat beolvasása egy helyen.

### 2. példa:
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A specific logical networks at a location based on a name.
```

Meghatározott logikai hálózatok beszerzése egy név alapján

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Szűrő
OData-szűrő paraméter

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Hely
Az erőforrás helye.

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
A logikai hálózat neve.

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

### -PassThru
Igaz érték visszaadása a parancs sikeressége után

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
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.
Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

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

### Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. models. IFabricAdminIdentity

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. FabricAdmin. modellek. Api20160501. ILogicalNetwork



## MEGJEGYZI

KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.

INPUTOBJECT <IFabricAdminIdentity> : Identity paraméter
  - `[Drive <String>]`: A tároló meghajtó neve.
  - `[EdgeGateway <String>]`: Az Edge-átjáró neve.
  - `[EdgeGatewayPool <String>]`: Az Edge Gateway-készlet neve.
  - `[FabricLocation <String>]`: Szövet helye.
  - `[FileShare <String>]`: A szövet-fájlmegosztás neve.
  - `[IPPool <String>]`: IP-készlet neve.
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[InfraRole <String>]`: Infrastrukturális szerepkör neve.
  - `[InfraRoleInstance <String>]`: Infrastruktúra-szerepkör példányának neve.
  - `[Location <String>]`: Az erőforrás helye.
  - `[LogicalNetwork <String>]`: A logikai hálózat neve.
  - `[LogicalSubnet <String>]`: A logikai alhálózat neve.
  - `[MacAddressPool <String>]`: A MAC-címkészlet neve.
  - `[Operation <String>]`: Műveleti azonosító.
  - `[ResourceGroupName <String>]`: Az erőforráscsoport neve.
  - `[ScaleUnit <String>]`: A méretarány neve.
  - `[ScaleUnitNode <String>]`: A Scale Unit csomópont neve.
  - `[SlbMuxInstance <String>]`: A SLB MUX példányának neve.
  - `[StoragePool <String>]`: Tároló neve.
  - `[StorageSubSystem <String>]`: A tárolási rendszer neve.
  - `[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.
  - `[Volume <String>]`: A tárolási mennyiség neve.

## KAPCSOLÓDÓ HIVATKOZÁSOK

