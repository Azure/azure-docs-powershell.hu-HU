---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 7abbe244e702c80f18d2c9e97236f74d60f094bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012485"
---
# <span data-ttu-id="34a8a-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="34a8a-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="34a8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="34a8a-103">Csatlakoztatott fürt törlése, a nyomon követhető erőforrás eltávolítása az Azure Resource Managerben (ARM).</span><span class="sxs-lookup"><span data-stu-id="34a8a-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="34a8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="34a8a-104">SYNTAX</span></span>

### <span data-ttu-id="34a8a-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34a8a-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="34a8a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="34a8a-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="34a8a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="34a8a-107">DESCRIPTION</span></span>
<span data-ttu-id="34a8a-108">Csatlakoztatott fürt törlése, a nyomon követhető erőforrás eltávolítása az Azure Resource Managerben (ARM).</span><span class="sxs-lookup"><span data-stu-id="34a8a-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="34a8a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="34a8a-109">EXAMPLES</span></span>

### <span data-ttu-id="34a8a-110">1. példa: Csatlakoztatott kumernetek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="34a8a-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="34a8a-111">Ez a parancs eltávolítja a csatlakoztatott kuberneteket</span><span class="sxs-lookup"><span data-stu-id="34a8a-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="34a8a-112">2. példa: Csatlakoztatott időhálózatok eltávolítása objektum alapján</span><span class="sxs-lookup"><span data-stu-id="34a8a-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="34a8a-113">Ez a parancs objektum szerint eltávolítja a csatlakoztatott kuberneteket</span><span class="sxs-lookup"><span data-stu-id="34a8a-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="34a8a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34a8a-114">PARAMETERS</span></span>

### <span data-ttu-id="34a8a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34a8a-115">-AsJob</span></span>
<span data-ttu-id="34a8a-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="34a8a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="34a8a-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="34a8a-117">-ClusterName</span></span>
<span data-ttu-id="34a8a-118">Annak a Kutbernetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="34a8a-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a8a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a8a-119">-DefaultProfile</span></span>
<span data-ttu-id="34a8a-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34a8a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a8a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34a8a-121">-InputObject</span></span>
<span data-ttu-id="34a8a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="34a8a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34a8a-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="34a8a-123">-KubeConfig</span></span>
<span data-ttu-id="34a8a-124">A kube config fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="34a8a-124">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a8a-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="34a8a-125">-KubeContext</span></span>
<span data-ttu-id="34a8a-126">Az aktuális gépről származó Kubaconfig környezet</span><span class="sxs-lookup"><span data-stu-id="34a8a-126">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a8a-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="34a8a-127">-NoWait</span></span>
<span data-ttu-id="34a8a-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="34a8a-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="34a8a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34a8a-129">-PassThru</span></span>
<span data-ttu-id="34a8a-130">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="34a8a-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="34a8a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a8a-131">-ResourceGroupName</span></span>
<span data-ttu-id="34a8a-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="34a8a-132">The name of the resource group.</span></span>
<span data-ttu-id="34a8a-133">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="34a8a-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a8a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34a8a-134">-SubscriptionId</span></span>
<span data-ttu-id="34a8a-135">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="34a8a-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a8a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34a8a-136">-Confirm</span></span>
<span data-ttu-id="34a8a-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="34a8a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a8a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a8a-138">-WhatIf</span></span>
<span data-ttu-id="34a8a-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="34a8a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34a8a-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34a8a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a8a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a8a-141">CommonParameters</span></span>
<span data-ttu-id="34a8a-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a8a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a8a-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34a8a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a8a-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34a8a-144">INPUTS</span></span>

### <span data-ttu-id="34a8a-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="34a8a-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="34a8a-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34a8a-146">OUTPUTS</span></span>

### <span data-ttu-id="34a8a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34a8a-147">System.Boolean</span></span>

## <span data-ttu-id="34a8a-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="34a8a-148">NOTES</span></span>

<span data-ttu-id="34a8a-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="34a8a-149">ALIASES</span></span>

<span data-ttu-id="34a8a-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="34a8a-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34a8a-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="34a8a-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34a8a-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34a8a-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34a8a-153">INPUTOBJECT: <IConnectedKubernetesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="34a8a-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34a8a-154">`[ClusterName <String>]`: Annak a Kubanetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="34a8a-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="34a8a-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="34a8a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34a8a-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="34a8a-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34a8a-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="34a8a-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="34a8a-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="34a8a-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="34a8a-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34a8a-159">RELATED LINKS</span></span>

