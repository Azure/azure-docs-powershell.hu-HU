---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162178"
---
# <span data-ttu-id="a36f0-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="a36f0-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="a36f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a36f0-102">SYNOPSIS</span></span>
<span data-ttu-id="a36f0-103">A megadott csatlakoztatott fürt tulajdonságait adja eredményül, beleértve a nevet, az identitást, a tulajdonságokat és a fürt további részleteit.</span><span class="sxs-lookup"><span data-stu-id="a36f0-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="a36f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a36f0-104">SYNTAX</span></span>

### <span data-ttu-id="a36f0-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a36f0-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a36f0-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="a36f0-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a36f0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a36f0-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a36f0-108">Lista</span><span class="sxs-lookup"><span data-stu-id="a36f0-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a36f0-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a36f0-109">DESCRIPTION</span></span>
<span data-ttu-id="a36f0-110">A megadott csatlakoztatott fürt tulajdonságait adja eredményül, beleértve a nevet, az identitást, a tulajdonságokat és a fürt további részleteit.</span><span class="sxs-lookup"><span data-stu-id="a36f0-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="a36f0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a36f0-111">EXAMPLES</span></span>

### <span data-ttu-id="a36f0-112">1. példa: Az összes csatlakoztatott időhálózat lekérte az előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="a36f0-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="a36f0-113">Ez a parancs az előfizetéshez kapcsolódó összes kubernetet lekérte.</span><span class="sxs-lookup"><span data-stu-id="a36f0-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="a36f0-114">2. példa: Az összes csatlakoztatott erőforráshálózat lekérte az erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="a36f0-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="a36f0-115">Ez a parancs az erőforráscsoport alatt az összes csatlakoztatott erőforráshálózatot lekérte.</span><span class="sxs-lookup"><span data-stu-id="a36f0-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="a36f0-116">3. példa: Csatlakoztatott kumernetes hálózat lekérte</span><span class="sxs-lookup"><span data-stu-id="a36f0-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="a36f0-117">Ez a parancs csatlakoztatott kuberneteket kap.</span><span class="sxs-lookup"><span data-stu-id="a36f0-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="a36f0-118">4. példa: Csatlakoztatott időhálózatok lekérte objektum szerint</span><span class="sxs-lookup"><span data-stu-id="a36f0-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="a36f0-119">Ez a parancs objektumról-objektumra lekért egy csatlakoztatott kubernetet.</span><span class="sxs-lookup"><span data-stu-id="a36f0-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="a36f0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a36f0-120">PARAMETERS</span></span>

### <span data-ttu-id="a36f0-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a36f0-121">-ClusterName</span></span>
<span data-ttu-id="a36f0-122">Annak a Kutbernetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="a36f0-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="a36f0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36f0-123">-DefaultProfile</span></span>
<span data-ttu-id="a36f0-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a36f0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a36f0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a36f0-125">-InputObject</span></span>
<span data-ttu-id="a36f0-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a36f0-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a36f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a36f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="a36f0-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a36f0-128">The name of the resource group.</span></span>
<span data-ttu-id="a36f0-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a36f0-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a36f0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a36f0-130">-SubscriptionId</span></span>
<span data-ttu-id="a36f0-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a36f0-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a36f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36f0-132">CommonParameters</span></span>
<span data-ttu-id="a36f0-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a36f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36f0-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a36f0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36f0-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a36f0-135">INPUTS</span></span>

### <span data-ttu-id="a36f0-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="a36f0-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="a36f0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a36f0-137">OUTPUTS</span></span>

### <span data-ttu-id="a36f0-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="a36f0-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="a36f0-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a36f0-139">NOTES</span></span>

<span data-ttu-id="a36f0-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a36f0-140">ALIASES</span></span>

<span data-ttu-id="a36f0-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a36f0-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a36f0-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a36f0-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a36f0-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a36f0-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a36f0-144">INPUTOBJECT: <IConnectedKubernetesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a36f0-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a36f0-145">`[ClusterName <String>]`: Annak a Kubanetes-fürtnek a neve, amelyen a lekért nevet hívták.</span><span class="sxs-lookup"><span data-stu-id="a36f0-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="a36f0-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a36f0-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a36f0-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a36f0-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a36f0-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a36f0-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="a36f0-149">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a36f0-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="a36f0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a36f0-150">RELATED LINKS</span></span>

