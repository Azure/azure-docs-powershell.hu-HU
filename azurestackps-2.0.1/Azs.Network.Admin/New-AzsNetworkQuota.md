---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015245"
---
# New-AzsNetworkQuota

## Áttekintés
Kvóta létrehozása vagy frissítése

## SZINTAXISA

### CreateExpanded (alapértelmezett)
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Létrehozása
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CreateViaIdentity
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CreateViaIdentityExpanded
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Leírás
Kvóta létrehozása vagy frissítése

## Példák

### --------------------------PÉLDA 1--------------------------
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

Hozzon létre egy új hálózati kvótát az összes alapértelmezett értékkel.

### --------------------------PÉLDA 2--------------------------
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
Új hálózati kvóta létrehozása a kvótával nem rendelkező alapértelmezett értékekkel



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

### -InputObject
Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
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
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxLoadBalancersPerSubscription
A bérlői előfizetések maximális száma a terheléselosztási szolgáltatásban.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxNicsPerSubscription
A bérlői előfizetésben használható hálózati adapterek maximális száma

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxPublicIpsPerSubscription
Nyilvános IP-címek maximális száma: a bérlői előfizetésben megadható.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxSecurityGroupsPerSubscription
Azoknak a biztonsági csoportoknak a maximális száma, amelyekhez bérlői előfizetés tud rendelkezni.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewayConnectionsPerSubscription
Virtuális hálózati átjárók maximális száma a bérlői előfizetésben.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewaysPerSubscription
Azoknak a virtuális hálózati átjáróknak a maximális száma, amelyeknek a bérlői előfizetése rendelkezésére áll.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVnetsPerSubscription
Azoknak a virtuális hálózatoknak a maximális száma, amelyekhez bérlői előfizetés tud rendelkezni.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name (név)
Az erőforrás neve.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Kvóta
Hálózati kvóta-erőforrás
A kivitelezéshez tekintse meg a kvóta tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -SubscriptionId
Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.
Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -Címke
A kulcs érték párok listája

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IQuota

### Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. models. INetworkAdminIdentity

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IQuota



## MEGJEGYZI

KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.

INPUTOBJECT <INetworkAdminIdentity> : Identity paraméter
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: Az erőforrás helye.
  - `[ResourceName <String>]`: Az erőforrás neve.
  - `[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

KVÓTA <IQuota> : hálózati kvóta-erőforrás.
  - `[Tag <IResourceTags>]`: A kulcsok érték párok listája.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[MaxLoadBalancersPerSubscription <Int64?>]`: A betöltők maximális száma a bérlői előfizetés rendelkezésére áll.
  - `[MaxNicsPerSubscription <Int64?>]`: A bérlői előfizetésben használható hálózati adapterek maximális száma
  - `[MaxPublicIpsPerSubscription <Int64?>]`: Nyilvános IP-címek maximális száma: a bérlői előfizetésben megadható.
  - `[MaxSecurityGroupsPerSubscription <Int64?>]`: A bérlői előfizetést tartalmazó biztonsági csoportok maximális száma
  - `[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: A virtuális hálózati átjárók által biztosított kapcsolatok maximális száma a bérlői előfizetésben.
  - `[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Azoknak a virtuális hálózati átjáróknak a maximális száma, amelyeknek a bérlői előfizetése rendelkezésére áll.
  - `[MaxVnetsPerSubscription <Int64?>]`: A virtuális hálózatok maximális száma, amely a bérlői előfizetést képes biztosítani.

## KAPCSOLÓDÓ HIVATKOZÁSOK

