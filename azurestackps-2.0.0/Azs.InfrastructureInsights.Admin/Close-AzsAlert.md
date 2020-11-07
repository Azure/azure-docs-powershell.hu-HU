---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842573"
---
# Close-AzsAlert

## Áttekintés
Bezárja az adott riasztást.

## SZINTAXISA

### CloseExpanded (alapértelmezett)
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Zárja be
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### CloseViaIdentity
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloseViaIdentityExpanded
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Leírás
Bezárja az adott riasztást.

## Példák

### Példa 1:
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

Riasztás megszüntetése név szerint

### 2. példa:
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

Riasztást az adatcsöveken keresztül zárhatja be.

## PARAMÉTEREK

### -Értesítés
Ez az objektum egy riasztási erőforrás.
A kivitelezéshez tekintse meg az ÉRTESÍTÉSi tulajdonságok című szakaszt, és hozzon létre egy ujjlenyomat-táblázatot.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -AlertId
Megkapja vagy beállítja a riasztás AZONOSÍTÓját.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -AlertProperty
A riasztás tulajdonságai

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ClosedByUserAlias
Az a felhasználó aliasneve, aki bezárta az értesítést.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ClosedTimestamp
Időbélyegző a riasztás lezárásakor.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -CreatedTimestamp
Időbélyegző a riasztás létrehozásakor

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

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

### -Leírás
A riasztás leírása.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -FaultId
Megkapja vagy beállítja a riasztás hibájának AZONOSÍTÓját.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -FaultTypeId
A riasztás hibájának típusa AZONOSÍTÓját kapja vagy állítja be.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -HasValidRemediationAction
Azt jelzi, hogy a riasztás visszaközvetíthető-e.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ImpactedResourceDisplayName
Az érintett elem megjelenített neve.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ImpactedResourceId
Az érintett elem erőforrás-AZONOSÍTÓjának beolvasása vagy beállítása.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
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
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -LastUpdatedTimestamp
Időbélyegző a riasztás utolsó frissítésekor.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Hely
A régió neve

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Location1
Az az Azure-terület, ahol az erőforrás él

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name (név)
A riasztás neve.

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Kármentesítés
Beolvassa vagy beállítja a riasztáshoz szükséges rendszergazdai szervizelési utasításokat.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
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
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceProviderRegistrationId
Megkapja vagy beállítja annak a szolgáltatásnak a regisztrációs AZONOSÍTÓját, amelyre a riasztás tartozik.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceRegistrationId
A riasztáshoz társított erőforrás regisztrációs AZONOSÍTÓjának beolvasása vagy beállítása.
Ha a riasztás nincs erőforráshoz társítva, az erőforrás-regisztrációs azonosító értéke null.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Súlyosság
A riasztás súlyossága.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -State (állami)
A riasztás állapota

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.
Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -Címke
Erőforrás-címkék.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Cím
Az érintett elem erőforrás-AZONOSÍTÓjának beolvasása vagy beállítása.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Felhasználó
A művelet végrehajtásához használt Felhasználónév.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. modellek. Api20160501. IAlert

### Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. modellek. Api20160501. IAlert



## MEGJEGYZI

KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.

RIASZTÁS <IAlert> : ez az objektum egy riasztási erőforrás.
  - `[Location <String>]`: Az Azure régió, ahol az erőforrás él
  - `[Tag <ITrackedResourceTags>]`: Erőforrás-címkék.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[AlertId <String>]`: Beolvassa vagy beállítja a riasztás AZONOSÍTÓját.
  - `[AlertProperty <IAlertModelAlertProperties>]`: A riasztás tulajdonságai.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[ClosedByUserAlias <String>]`: Az a felhasználó aliasneve, aki bezárta az értesítést.
  - `[ClosedTimestamp <String>]`: Időbélyegző, ha a riasztás be van zárva.
  - `[CreatedTimestamp <String>]`: Időbélyegző a riasztás létrehozásakor
  - `[Description <IDictionary[]>]`: A riasztás leírása.
  - `[FaultId <String>]`: Beolvassa vagy beállítja a riasztás hibájának AZONOSÍTÓját.
  - `[FaultTypeId <String>]`: Beolvassa vagy beállítja a riasztás hibájának típusát AZONOSÍTÓját.
  - `[HasValidRemediationAction <Boolean?>]`: Azt jelzi, hogy a riasztás visszaközvetíthető-e.
  - `[ImpactedResourceDisplayName <String>]`: Az ütközésben lévő elem megjelenítendő neve.
  - `[ImpactedResourceId <String>]`: Az érintett elem erőforrás-AZONOSÍTÓjának beolvasása vagy beállítása.
  - `[LastUpdatedTimestamp <String>]`: Időbélyegző a riasztás utolsó frissítésekor.
  - `[Remediation <IDictionary[]>]`: A riasztáshoz beolvassa vagy beállítja a rendszergazdai felhasználóbarát szervizelési utasításokat.
  - `[ResourceProviderRegistrationId <String>]`: Beadja vagy beállítja annak a szolgáltatásnak a regisztrációs AZONOSÍTÓját, amelyre a riasztás tartozik.
  - `[ResourceRegistrationId <String>]`: A riasztáshoz társított erőforrás regisztrációs AZONOSÍTÓjának beolvasása vagy beállítása. Ha a riasztás nincs erőforráshoz társítva, az erőforrás-regisztrációs azonosító értéke null.
  - `[Severity <String>]`: A riasztás súlyossága.
  - `[State <String>]`: A riasztás állapota.
  - `[Title <String>]`: Az érintett elem erőforrás-AZONOSÍTÓjának beolvasása vagy beállítása.

INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity paraméter
  - `[AlertName <String>]`: A riasztás neve.
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: A régió neve
  - `[ResourceGroupName <String>]`: Az erőforráscsoport neve.
  - `[ResourceRegistrationId <String>]`: Erőforrás-regisztrációs azonosító.
  - `[ServiceHealth <String>]`: Szolgáltatás állapota név.
  - `[ServiceRegistrationId <String>]`: Szolgáltatás-regisztrációs azonosító.
  - `[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

## KAPCSOLÓDÓ HIVATKOZÁSOK

