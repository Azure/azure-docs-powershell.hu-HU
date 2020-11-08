---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187192"
---
# Unregister-AzStackHCI

## Áttekintés
Unregister-AzStackHCI törli a helyszíni fürtöt képviselő Microsoft. AzureStackHCI felhőalapú erőforrást, és a helyszíni fürtöt eltávolítja az Azure rendszerből.
A fürtben rendelkezésre álló regisztrált adatok a fürt regisztrációjának törlésére szolgálnak, ha nincs paraméter átadva.

## SZINTAXISA

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Unregister-AzStackHCI törli a helyszíni fürtöt képviselő Microsoft. AzureStackHCI felhőalapú erőforrást, és a helyszíni fürtöt eltávolítja az Azure rendszerből.
A fürtben rendelkezésre álló regisztrált adatok a fürt regisztrációjának törlésére szolgálnak, ha nincs paraméter átadva.

## Példák

### PÉLDA 1
```
Invoking on one of the cluster node
```

C:\PS \> unregister-AzStackHCI eredmény: siker

### 2. PÉLDA
```
Invoking from the management node
```

C:\PS \> unregister-AzStackHCI-számítógép_neve ClusterNode1 result: Success (siker)

### 3. PÉLDA
```
Invoking from WAC
```

C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourcename DemoHCICluster3-ResourceGroupName DemoHCIRG – megerősítés: $false eredmény: siker

### 4. PÉLDA
```
Invoking with all the parameters
```

C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-resourcename HciCluster1-bérlői azonosító megkeresése "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName-HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-számítógép_neve node1hci-hitelesítő adatok Get-Credential eredmény: siker

## PARAMÉTEREK

### -SubscriptionId
Az Azure-előfizetést adja meg az erőforrás létrehozásához

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Az Azure-ban létrehozott erőforrás erőforrásának nevét adja meg.
Ha nem adja meg, akkor a helyszíni fürt nevét használja a rendszer.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bérlői azonosító megkeresése
Az Azure bérlői azonosító megkeresése adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az Azure Resource Group nevet adja meg.
Ha nem adja meg \<LocalClusterName\> a-RG nevet, a program erőforrás-csoportként használja.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
A ARM hozzáférési tokent adja meg.
A GraphAccessToken és a AccountId együtt az Azure interaktív bejelentkezést is el kell kerülnie.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
A Graph Access-tokent adja meg.
A ArmAccessToken és a AccountId együtt az Azure interaktív bejelentkezést is el kell kerülnie.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
A ARM hozzáférési tokent adja meg.
A ArmAccessToken és a GraphAccessToken együtt az Azure interaktív bejelentkezést is el kell kerülnie.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Az Azure-környezetet adja meg.
Az alapértelmezett érték a AzureCloud.
Az érvényes értékek a következők AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Számítógépnév
A helyszíni fürtökben az Azure rendszerhez regisztrált fürtcsomópont egyik csomópontját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hitelesítő adatok
A számítógépnév hitelesítő adatait adja meg.
Az alapértelmezett beállítás a parancsmagot végrehajtó jelenlegi felhasználó.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

## KIMENETEK

### PSCustomObject. Az PSCustomObject az alábbi tulajdonságokat számítja ki.
### Eredmény: sikeres vagy sikertelen vagy lemondott.
## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
