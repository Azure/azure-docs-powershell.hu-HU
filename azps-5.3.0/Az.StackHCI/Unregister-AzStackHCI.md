---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374190"
---
# <span data-ttu-id="b6749-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="b6749-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="b6749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6749-102">SYNOPSIS</span></span>
<span data-ttu-id="b6749-103">Unregister-AzStackHCI törli a Microsoft.AzureStackHCI felhőbeli erőforrást, amely a helyi fürtöt képviseli, és törli a helyi fürt regisztrációját az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="b6749-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="b6749-104">A fürtön elérhető regisztrált információk a fürt regisztrációjának a visszaszabadulnak, ha nem ad át paramétereket.</span><span class="sxs-lookup"><span data-stu-id="b6749-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="b6749-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6749-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6749-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6749-106">DESCRIPTION</span></span>
<span data-ttu-id="b6749-107">Unregister-AzStackHCI törli a Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtöt képviseli, és törli a helyi fürt regisztrációját az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="b6749-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="b6749-108">A fürtön elérhető regisztrált információk a fürt regisztrációjának a visszaszabadulnak, ha nem ad át paramétereket.</span><span class="sxs-lookup"><span data-stu-id="b6749-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="b6749-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6749-109">EXAMPLES</span></span>

### <span data-ttu-id="b6749-110">1. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b6749-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="b6749-111">C:\PS \> Unregister-AzStackHCI eredmény: Success</span><span class="sxs-lookup"><span data-stu-id="b6749-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="b6749-112">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b6749-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="b6749-113">C:\PS \> Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span><span class="sxs-lookup"><span data-stu-id="b6749-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="b6749-114">3. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b6749-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="b6749-115">C:\PS \> Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer.. ere= -GraphAccessToken acyee.. rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span><span class="sxs-lookup"><span data-stu-id="b6749-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="b6749-116">4. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b6749-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="b6749-117">C:\PS \> Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer.. ere= -GraphAccessToken acee.. rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span><span class="sxs-lookup"><span data-stu-id="b6749-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="b6749-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6749-118">PARAMETERS</span></span>

### <span data-ttu-id="b6749-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="b6749-119">-AccountId</span></span>
<span data-ttu-id="b6749-120">Megadja a ARM hozzáférési jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="b6749-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="b6749-121">Ha ezt az ArmAccessToken és a GraphAccessToken mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezését.</span><span class="sxs-lookup"><span data-stu-id="b6749-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="b6749-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="b6749-122">-ArmAccessToken</span></span>
<span data-ttu-id="b6749-123">Megadja a ARM hozzáférési jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="b6749-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="b6749-124">Ha ezt a GraphAccessToken és az AccountId érték mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="b6749-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="b6749-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="b6749-125">-ComputerName</span></span>
<span data-ttu-id="b6749-126">Az Azure-ba regisztrált, a környezetben található fürtben található fürtcsomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6749-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="b6749-127">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b6749-127">-Credential</span></span>
<span data-ttu-id="b6749-128">A Számítógépnév hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6749-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="b6749-129">Az alapértelmezett érték az a felhasználó, aki végrehajtja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b6749-129">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="b6749-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b6749-130">-EnvironmentName</span></span>
<span data-ttu-id="b6749-131">Az Azure-környezetet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b6749-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="b6749-132">Az alapértelmezett érték az AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="b6749-132">Default is AzureCloud.</span></span>
<span data-ttu-id="b6749-133">Érvényes értékek: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="b6749-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="b6749-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="b6749-134">-GraphAccessToken</span></span>
<span data-ttu-id="b6749-135">A Graph-hozzáférési jogkivonatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6749-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="b6749-136">Ha ezt az ArmAccessToken és az AccountId érték mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="b6749-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="b6749-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6749-137">-ResourceGroupName</span></span>
<span data-ttu-id="b6749-138">Az Azure Erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6749-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="b6749-139">Ha nincs \<LocalClusterName\> megadva , akkor a -rg lesz az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6749-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="b6749-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b6749-140">-ResourceName</span></span>
<span data-ttu-id="b6749-141">Az Azure-ban létrehozott erőforrás erőforrásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6749-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="b6749-142">Ha nincs megadva, akkor a fürt neve a megadott időpontban történik.</span><span class="sxs-lookup"><span data-stu-id="b6749-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="b6749-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6749-143">-SubscriptionId</span></span>
<span data-ttu-id="b6749-144">Megadja az erőforrás létrehozásához szükséges Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b6749-144">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="b6749-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b6749-145">-TenantId</span></span>
<span data-ttu-id="b6749-146">Az Azure TenantId tulajdonságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6749-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="b6749-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="b6749-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="b6749-148">Interaktív böngészőablak helyett használjon eszközkód-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="b6749-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="b6749-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6749-149">-Confirm</span></span>
<span data-ttu-id="b6749-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b6749-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6749-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6749-151">-WhatIf</span></span>
<span data-ttu-id="b6749-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b6749-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6749-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6749-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6749-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6749-154">CommonParameters</span></span>
<span data-ttu-id="b6749-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6749-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6749-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6749-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6749-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6749-157">INPUTS</span></span>

## <span data-ttu-id="b6749-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6749-158">OUTPUTS</span></span>

### <span data-ttu-id="b6749-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="b6749-159">PSCustomObject.</span></span> <span data-ttu-id="b6749-160">A PSCustomObject tulajdonságot követő tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b6749-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="b6749-161">Eredmény: Sikeres, sikertelen vagy visszavont.</span><span class="sxs-lookup"><span data-stu-id="b6749-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="b6749-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6749-162">NOTES</span></span>

## <span data-ttu-id="b6749-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6749-163">RELATED LINKS</span></span>
