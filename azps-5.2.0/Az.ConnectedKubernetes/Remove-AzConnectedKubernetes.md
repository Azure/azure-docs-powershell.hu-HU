---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323690"
---
# <span data-ttu-id="7b983-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="7b983-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="7b983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b983-102">SYNOPSIS</span></span>
<span data-ttu-id="7b983-103">Csatlakoztatott fürt törlése, a nyomon követhető erőforrás eltávolítása az Azure Resource Managerben (ARM).</span><span class="sxs-lookup"><span data-stu-id="7b983-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="7b983-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b983-104">SYNTAX</span></span>

### <span data-ttu-id="7b983-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b983-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b983-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7b983-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7b983-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b983-107">DESCRIPTION</span></span>
<span data-ttu-id="7b983-108">Csatlakoztatott fürt törlése, a nyomon követhető erőforrás eltávolítása az Azure Resource Managerben (ARM).</span><span class="sxs-lookup"><span data-stu-id="7b983-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="7b983-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b983-109">EXAMPLES</span></span>

### <span data-ttu-id="7b983-110">1. példa: Csatlakoztatott kumernetek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7b983-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="7b983-111">Ez a parancs eltávolítja a csatlakoztatott kuberneteket</span><span class="sxs-lookup"><span data-stu-id="7b983-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="7b983-112">2. példa: Csatlakoztatott időhálózatok eltávolítása objektum alapján</span><span class="sxs-lookup"><span data-stu-id="7b983-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="7b983-113">Ez a parancs objektum szerint eltávolítja a csatlakoztatott kuberneteket</span><span class="sxs-lookup"><span data-stu-id="7b983-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="7b983-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b983-114">PARAMETERS</span></span>

### <span data-ttu-id="7b983-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b983-115">-AsJob</span></span>
<span data-ttu-id="7b983-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="7b983-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7b983-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7b983-117">-ClusterName</span></span>
<span data-ttu-id="7b983-118">Annak a Kutbernetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="7b983-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="7b983-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b983-119">-DefaultProfile</span></span>
<span data-ttu-id="7b983-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b983-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b983-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b983-121">-InputObject</span></span>
<span data-ttu-id="7b983-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7b983-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b983-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="7b983-123">-KubeConfig</span></span>
<span data-ttu-id="7b983-124">A kube config fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="7b983-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="7b983-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="7b983-125">-KubeContext</span></span>
<span data-ttu-id="7b983-126">Az aktuális gépről származó Kubaconfig környezet</span><span class="sxs-lookup"><span data-stu-id="7b983-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="7b983-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7b983-127">-NoWait</span></span>
<span data-ttu-id="7b983-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="7b983-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7b983-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b983-129">-PassThru</span></span>
<span data-ttu-id="7b983-130">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="7b983-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7b983-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b983-131">-ResourceGroupName</span></span>
<span data-ttu-id="7b983-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7b983-132">The name of the resource group.</span></span>
<span data-ttu-id="7b983-133">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="7b983-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7b983-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b983-134">-SubscriptionId</span></span>
<span data-ttu-id="7b983-135">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7b983-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7b983-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b983-136">-Confirm</span></span>
<span data-ttu-id="7b983-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7b983-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b983-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b983-138">-WhatIf</span></span>
<span data-ttu-id="7b983-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7b983-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b983-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b983-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b983-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b983-141">CommonParameters</span></span>
<span data-ttu-id="7b983-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b983-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b983-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b983-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b983-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b983-144">INPUTS</span></span>

### <span data-ttu-id="7b983-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="7b983-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="7b983-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b983-146">OUTPUTS</span></span>

### <span data-ttu-id="7b983-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b983-147">System.Boolean</span></span>

## <span data-ttu-id="7b983-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b983-148">NOTES</span></span>

<span data-ttu-id="7b983-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7b983-149">ALIASES</span></span>

<span data-ttu-id="7b983-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7b983-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b983-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7b983-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b983-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b983-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b983-153">INPUTOBJECT: <IConnectedKubernetesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7b983-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b983-154">`[ClusterName <String>]`: Annak a Kubanetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="7b983-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="7b983-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7b983-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b983-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7b983-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7b983-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="7b983-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="7b983-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7b983-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="7b983-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b983-159">RELATED LINKS</span></span>

