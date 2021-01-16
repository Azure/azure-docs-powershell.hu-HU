---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344741"
---
# <span data-ttu-id="66e31-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="66e31-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="66e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66e31-102">SYNOPSIS</span></span>
<span data-ttu-id="66e31-103">A megadott csatlakoztatott fürt tulajdonságait adja eredményül, beleértve a nevet, az identitást, a tulajdonságokat és a fürt további részleteit.</span><span class="sxs-lookup"><span data-stu-id="66e31-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="66e31-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66e31-104">SYNTAX</span></span>

### <span data-ttu-id="66e31-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66e31-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66e31-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="66e31-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66e31-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="66e31-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="66e31-108">Lista</span><span class="sxs-lookup"><span data-stu-id="66e31-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="66e31-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66e31-109">DESCRIPTION</span></span>
<span data-ttu-id="66e31-110">A megadott csatlakoztatott fürt tulajdonságait adja eredményül, beleértve a nevet, az identitást, a tulajdonságokat és a fürt további részleteit.</span><span class="sxs-lookup"><span data-stu-id="66e31-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="66e31-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66e31-111">EXAMPLES</span></span>

### <span data-ttu-id="66e31-112">1. példa: Az összes csatlakoztatott időhálózat lekérte az előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="66e31-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="66e31-113">Ez a parancs az előfizetéshez kapcsolódó összes kubernetet lekérte.</span><span class="sxs-lookup"><span data-stu-id="66e31-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="66e31-114">2. példa: Az összes csatlakoztatott erőforráshálózat lekérte az erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="66e31-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="66e31-115">Ez a parancs az erőforráscsoport alatt az összes csatlakoztatott erőforráshálózatot lekérte.</span><span class="sxs-lookup"><span data-stu-id="66e31-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="66e31-116">3. példa: Csatlakoztatott kumernetes hálózat lekérte</span><span class="sxs-lookup"><span data-stu-id="66e31-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="66e31-117">Ez a parancs csatlakoztatott kuberneteket kap.</span><span class="sxs-lookup"><span data-stu-id="66e31-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="66e31-118">4. példa: Csatlakoztatott időhálózatok lekérte objektum szerint</span><span class="sxs-lookup"><span data-stu-id="66e31-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="66e31-119">Ez a parancs objektumról-objektumra lekért egy csatlakoztatott kubernetet.</span><span class="sxs-lookup"><span data-stu-id="66e31-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="66e31-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66e31-120">PARAMETERS</span></span>

### <span data-ttu-id="66e31-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="66e31-121">-ClusterName</span></span>
<span data-ttu-id="66e31-122">Annak a Kutbernetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="66e31-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e31-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e31-123">-DefaultProfile</span></span>
<span data-ttu-id="66e31-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66e31-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66e31-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66e31-125">-InputObject</span></span>
<span data-ttu-id="66e31-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="66e31-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66e31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e31-127">-ResourceGroupName</span></span>
<span data-ttu-id="66e31-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="66e31-128">The name of the resource group.</span></span>
<span data-ttu-id="66e31-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="66e31-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e31-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66e31-130">-SubscriptionId</span></span>
<span data-ttu-id="66e31-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66e31-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e31-132">CommonParameters</span></span>
<span data-ttu-id="66e31-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66e31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e31-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66e31-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e31-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66e31-135">INPUTS</span></span>

### <span data-ttu-id="66e31-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="66e31-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="66e31-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66e31-137">OUTPUTS</span></span>

### <span data-ttu-id="66e31-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="66e31-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="66e31-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66e31-139">NOTES</span></span>

<span data-ttu-id="66e31-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="66e31-140">ALIASES</span></span>

<span data-ttu-id="66e31-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="66e31-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66e31-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="66e31-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66e31-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66e31-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66e31-144">INPUTOBJECT: <IConnectedKubernetesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="66e31-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66e31-145">`[ClusterName <String>]`: Annak a Kubanetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="66e31-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="66e31-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="66e31-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66e31-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="66e31-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="66e31-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="66e31-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="66e31-149">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66e31-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="66e31-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66e31-150">RELATED LINKS</span></span>

