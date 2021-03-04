---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: 3f38a11cd5d4a124e7db7a99422239f73cbe96dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930714"
---
# <span data-ttu-id="49dc5-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="49dc5-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="49dc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="49dc5-103">Unregister-AzStackHCI törli a Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtöt képviseli, és törli a helyi fürt regisztrációját az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="49dc5-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="49dc5-104">Ha nem ad át paramétereket, a fürtön elérhető regisztrált információk a fürt regisztrációjának a nevére használatosak.</span><span class="sxs-lookup"><span data-stu-id="49dc5-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="49dc5-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49dc5-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49dc5-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49dc5-106">DESCRIPTION</span></span>
<span data-ttu-id="49dc5-107">Unregister-AzStackHCI törli a Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtöt képviseli, és törli a helyi fürt regisztrációját az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="49dc5-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="49dc5-108">Ha nem ad át paramétereket, a fürtön elérhető regisztrált információk a fürt regisztrációjának a nevére használatosak.</span><span class="sxs-lookup"><span data-stu-id="49dc5-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="49dc5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49dc5-109">EXAMPLES</span></span>

### <span data-ttu-id="49dc5-110">1. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="49dc5-110">EXAMPLE 1</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
<span data-ttu-id="49dc5-111">Invoking on one the cluster node</span><span class="sxs-lookup"><span data-stu-id="49dc5-111">Invoking on one of the cluster node</span></span>

### <span data-ttu-id="49dc5-112">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="49dc5-112">EXAMPLE 2</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
<span data-ttu-id="49dc5-113">Invoking from the management node</span><span class="sxs-lookup"><span data-stu-id="49dc5-113">Invoking from the management node</span></span>

### <span data-ttu-id="49dc5-114">3. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="49dc5-114">EXAMPLE 3</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
<span data-ttu-id="49dc5-115">Invoking from WAC</span><span class="sxs-lookup"><span data-stu-id="49dc5-115">Invoking from WAC</span></span>

### <span data-ttu-id="49dc5-116">4. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="49dc5-116">EXAMPLE 4</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
<span data-ttu-id="49dc5-117">Invoking with all the parameters</span><span class="sxs-lookup"><span data-stu-id="49dc5-117">Invoking with all the parameters</span></span>

## <span data-ttu-id="49dc5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49dc5-118">PARAMETERS</span></span>

### <span data-ttu-id="49dc5-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="49dc5-119">-AccountId</span></span>
<span data-ttu-id="49dc5-120">Megadja a ARM hozzáférési jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="49dc5-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="49dc5-121">Ha ezt az ArmAccessToken és a GraphAccessToken mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="49dc5-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="49dc5-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="49dc5-122">-ArmAccessToken</span></span>
<span data-ttu-id="49dc5-123">Megadja a ARM hozzáférési jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="49dc5-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="49dc5-124">Ha ezt a GraphAccessToken és az AccountId érték mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="49dc5-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="49dc5-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="49dc5-125">-ComputerName</span></span>
<span data-ttu-id="49dc5-126">Az Azure-ba regisztrált, a környezetben található fürtben található egyik fürtcsomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dc5-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="49dc5-127">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="49dc5-127">-Credential</span></span>
<span data-ttu-id="49dc5-128">A Számítógépnév hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dc5-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="49dc5-129">Az alapértelmezett érték az a felhasználó, aki végrehajtja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="49dc5-129">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="49dc5-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="49dc5-130">-EnvironmentName</span></span>
<span data-ttu-id="49dc5-131">Az Azure-környezetet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="49dc5-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="49dc5-132">Az alapértelmezett érték az AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="49dc5-132">Default is AzureCloud.</span></span>
<span data-ttu-id="49dc5-133">Érvényes értékek: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="49dc5-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="49dc5-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="49dc5-134">-GraphAccessToken</span></span>
<span data-ttu-id="49dc5-135">A Graph-hozzáférési jogkivonatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dc5-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="49dc5-136">Ha ezt az ArmAccessToken és az AccountId beállítással együtt adja meg, azzal elkerüli az Azure interaktív bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="49dc5-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="49dc5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49dc5-137">-ResourceGroupName</span></span>
<span data-ttu-id="49dc5-138">Az Azure Erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dc5-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="49dc5-139">Ha nincs megadva ,rg, akkor az erőforráscsoport \<LocalClusterName\> neve lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="49dc5-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="49dc5-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="49dc5-140">-ResourceName</span></span>
<span data-ttu-id="49dc5-141">Az Azure-ban létrehozott erőforrás erőforrásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dc5-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="49dc5-142">Ha nincs megadva, akkor a fürt neve a megadott időpontban történik.</span><span class="sxs-lookup"><span data-stu-id="49dc5-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="49dc5-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49dc5-143">-SubscriptionId</span></span>
<span data-ttu-id="49dc5-144">Megadja az erőforrás létrehozásához szükséges Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="49dc5-144">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="49dc5-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="49dc5-145">-TenantId</span></span>
<span data-ttu-id="49dc5-146">Az Azure TenantId tulajdonságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="49dc5-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="49dc5-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="49dc5-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="49dc5-148">Interaktív böngészőablak helyett használjon eszközkód-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="49dc5-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="49dc5-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49dc5-149">-Confirm</span></span>
<span data-ttu-id="49dc5-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49dc5-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49dc5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49dc5-151">-WhatIf</span></span>
<span data-ttu-id="49dc5-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49dc5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49dc5-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49dc5-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49dc5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49dc5-154">CommonParameters</span></span>
<span data-ttu-id="49dc5-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49dc5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49dc5-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49dc5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49dc5-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49dc5-157">INPUTS</span></span>

## <span data-ttu-id="49dc5-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49dc5-158">OUTPUTS</span></span>

### <span data-ttu-id="49dc5-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="49dc5-159">PSCustomObject.</span></span> <span data-ttu-id="49dc5-160">A PSCustomObject tulajdonságot követő tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="49dc5-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="49dc5-161">Eredmény: Sikeres, sikertelen vagy visszavont.</span><span class="sxs-lookup"><span data-stu-id="49dc5-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="49dc5-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49dc5-162">NOTES</span></span>

## <span data-ttu-id="49dc5-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49dc5-163">RELATED LINKS</span></span>
