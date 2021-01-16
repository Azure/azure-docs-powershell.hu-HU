---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349914"
---
# Unregister-AzStackHCI

## SYNOPSIS
Unregister-AzStackHCI törli a Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtöt képviseli, és törli a helyi fürt regisztrációját az Azure-ral.
Ha nem ad át paramétereket, a fürtön elérhető regisztrált információk a fürt regisztrációjának a nevére használatosak.

## SZINTAXIS

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Unregister-AzStackHCI törli a Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtöt képviseli, és törli a helyi fürt regisztrációját az Azure-ral.
Ha nem ad át paramétereket, a fürtön elérhető regisztrált információk a fürt regisztrációjának a nevére használatosak.

## PÉLDÁK

### 1. PÉLDA
```
Invoking on one of the cluster node
```

C:\PS \> Unregister-AzStackHCI eredmény: Success

### 2. PÉLDA
```
Invoking from the management node
```

C:\PS \> Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success

### 3. PÉLDA
```
Invoking from WAC
```

C:\PS \> Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer.. ere= -GraphAccessToken acyee.. rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success

### 4. PÉLDA
```
Invoking with all the parameters
```

C:\PS \> Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer.. ere= -GraphAccessToken acee.. rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success

## PARAMETERS

### -AccountId
Megadja a ARM hozzáférési jogkivonatot.
Ha ezt az ArmAccessToken és a GraphAccessToken mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezést.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
Megadja a ARM hozzáférési jogkivonatot.
Ha ezt a GraphAccessToken és az AccountId érték mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezést.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Az Azure-ba regisztrált, a környezetben található fürtben található egyik fürtcsomópontot adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hitelesítő adatok
A Számítógépnév hitelesítő adatait adja meg.
Az alapértelmezett érték az a felhasználó, aki végrehajtja a parancsmagot.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Az Azure-környezetet határozza meg.
Az alapértelmezett érték az AzureCloud.
Érvényes értékek: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
A Graph-hozzáférési jogkivonatot adja meg.
Ha ezt az ArmAccessToken és az AccountId beállítással együtt adja meg, azzal elkerüli az Azure interaktív bejelentkezést.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az Azure Erőforráscsoport nevét adja meg.
Ha nincs megadva ,rg, akkor az erőforráscsoport \<LocalClusterName\> neve lesz használatos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Az Azure-ban létrehozott erőforrás erőforrásnevét adja meg.
Ha nincs megadva, akkor a fürt neve a megadott időpontban történik.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Megadja az erőforrás létrehozásához szükséges Azure-előfizetést.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Az Azure TenantId tulajdonságot adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication
Interaktív böngészőablak helyett használjon eszközkód-hitelesítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### PSCustomObject. A PSCustomObject tulajdonságot követő tulajdonságokat adja eredményül.
### Eredmény: Sikeres, sikertelen vagy visszavont.
## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
