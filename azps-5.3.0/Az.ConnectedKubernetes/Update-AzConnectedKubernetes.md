---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477613"
---
# <span data-ttu-id="6cb42-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="6cb42-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="6cb42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb42-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb42-103">API a csatlakoztatott fürterőforrás bizonyos tulajdonságainak frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="6cb42-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="6cb42-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cb42-104">SYNTAX</span></span>

### <span data-ttu-id="6cb42-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cb42-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6cb42-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6cb42-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cb42-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cb42-107">DESCRIPTION</span></span>
<span data-ttu-id="6cb42-108">API a csatlakoztatott fürterőforrás bizonyos tulajdonságainak frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="6cb42-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="6cb42-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cb42-109">EXAMPLES</span></span>

### <span data-ttu-id="6cb42-110">1. példa: Csatlakoztatott rendszernetek frissítése</span><span class="sxs-lookup"><span data-stu-id="6cb42-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6cb42-111">Ez a parancs frissíti a csatlakoztatott rendszerhálózatokat.</span><span class="sxs-lookup"><span data-stu-id="6cb42-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="6cb42-112">2. példa: Csatlakoztatott kumernetek frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="6cb42-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6cb42-113">Ez a parancs objektum szerint frissíti a csatlakoztatott rendszerhálózatokat.</span><span class="sxs-lookup"><span data-stu-id="6cb42-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="6cb42-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cb42-114">PARAMETERS</span></span>

### <span data-ttu-id="6cb42-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6cb42-115">-ClusterName</span></span>
<span data-ttu-id="6cb42-116">Annak a Kutbernetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="6cb42-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb42-117">-DefaultProfile</span></span>
<span data-ttu-id="6cb42-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cb42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cb42-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cb42-119">-InputObject</span></span>
<span data-ttu-id="6cb42-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6cb42-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb42-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb42-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cb42-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cb42-122">The name of the resource group.</span></span>
<span data-ttu-id="6cb42-123">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6cb42-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb42-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cb42-124">-SubscriptionId</span></span>
<span data-ttu-id="6cb42-125">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cb42-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb42-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="6cb42-126">-Tag</span></span>
<span data-ttu-id="6cb42-127">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="6cb42-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb42-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cb42-128">-Confirm</span></span>
<span data-ttu-id="6cb42-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cb42-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb42-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb42-130">-WhatIf</span></span>
<span data-ttu-id="6cb42-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6cb42-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cb42-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cb42-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb42-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb42-133">CommonParameters</span></span>
<span data-ttu-id="6cb42-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb42-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb42-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cb42-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb42-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cb42-136">INPUTS</span></span>

### <span data-ttu-id="6cb42-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="6cb42-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="6cb42-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb42-138">OUTPUTS</span></span>

### <span data-ttu-id="6cb42-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="6cb42-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="6cb42-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cb42-140">NOTES</span></span>

<span data-ttu-id="6cb42-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6cb42-141">ALIASES</span></span>

<span data-ttu-id="6cb42-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6cb42-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cb42-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6cb42-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cb42-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cb42-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cb42-145">INPUTOBJECT: <IConnectedKubernetesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6cb42-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cb42-146">`[ClusterName <String>]`: Annak a Kubanetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="6cb42-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="6cb42-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6cb42-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cb42-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6cb42-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6cb42-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="6cb42-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="6cb42-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cb42-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6cb42-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cb42-151">RELATED LINKS</span></span>

