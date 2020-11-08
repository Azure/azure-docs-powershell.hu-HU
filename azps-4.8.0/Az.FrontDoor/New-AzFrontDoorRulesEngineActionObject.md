---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182776"
---
# New-AzFrontDoorRulesEngineActionObject

## Áttekintés
PSRulesEngineAction objektum létrehozása szabály-végrehajtó szabály létrehozásához.

## SZINTAXISA

### ByFieldsWithForwardingParameterSet
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFieldsWithRedirectParameterSet
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
PSRulesEngineAction objektum létrehozása szabály-végrehajtó szabály létrehozásához. 

A parancsmag "New-AzFrontDoorHeaderActionObject" paranccsal PSHeaderObjects hozhat létre a "-RequestHeaderActions" és a "-ResponseHeaderActions" paraméterekkel.

## Példák

### Példa 1
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

A szabályok motorjának létrehozása és a szabályok megadására szolgáló műveletek megtekintése

## PARAMÉTEREK

### -BackendPoolName
Annak a BackendPool a neve, amelyre a szabály vonatkozik

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomForwardingPath
A szabály által kiválasztott erőforrás-elérési utak átírásához használt egyéni elérési út.
Hagyja üresen a bejövő elérési út használatát.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomFragment
Az átirányítási URL-címhez hozzáadni kívánt részlet
A töredék a # után elkerülő URL-cím része.
Ne szerepeljen a #.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomHost
Állomás átirányítását.
Hagyja üresen a bejövő állomás rendeltetési állomásként való használatát.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomPath
Az átirányítás teljes elérési útja.
Az elérési út nem lehet üres, és a/értékkel kell kezdődnie.
Hagyja üresen a bejövő út rendeltetési útvonalként való használatát.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomQueryString
Az átirányítási URL-címben elhelyezni kívánt lekérdezési karakterláncok halmaza.
Beállítás: az érték felülírhatja a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.
A lekérdezési karakterláncnak formátumban kell lennie \<key\> = \<value\> .
Az első?
a & automatikusan felveszi a program, hogy ne szerepeljenek rajtuk, de a lekérdezési karakterláncokat külön-külön kell kiválasztania a &.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DynamicCompression
Engedélyezi-e a dinamikus tömörítést a gyorsítótárazott tartalomhoz.
Az alapértelmezett érték engedélyezve

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCaching
Engedélyezi-e az útvonal gyorsítótárazását.
Az alapértelmezett érték a hamis

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForwardingProtocol
A protokoll ezt a szabályt fogja használni a forgalom backend-re való továbbításakor.
Az alapértelmezett érték a MatchRequest

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontDoorName
Annak a bejárati ajtónak a neve, amelyhez ez a művelettervi szabály tartozik.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryParameterStripDirective
Az URL-lekérdezési fogalmak kezelése a gyorsítótár-kulcs alakításakor.
Az alapértelmezett érték a StripAll

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectProtocol
Annak a helynek a protokollja, ahol a forgalmat átirányítják.
Az alapértelmezett érték a MatchRequest

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectType
Az átirányítás típusa: a szabály a forgalom átirányításakor használatos.
Az alapértelmezett érték áthelyezve

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestHeaderAction
Annak a fejléc-műveleteknek a listája, amelyeket a AFD-ról a származási kérelemből kell alkalmazni.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-névnek a neve, amelyet a RoutingRule fog létrehozni.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResponseHeaderAction
A AFD és az ügyfél közötti válaszból az adott választól alkalmazni kívánt fejléc-műveletek listája.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. FrontDoor. models. PSRulesEngineAction

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
