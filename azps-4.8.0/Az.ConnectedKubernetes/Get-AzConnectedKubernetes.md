---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183396"
---
# <span data-ttu-id="711aa-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="711aa-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="711aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="711aa-102">SYNOPSIS</span></span>
<span data-ttu-id="711aa-103">A megadott csatlakoztatott fürt tulajdonságait adja meg, többek között a nevet, identitást, tulajdonságokat és a fürt további részleteit.</span><span class="sxs-lookup"><span data-stu-id="711aa-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="711aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="711aa-104">SYNTAX</span></span>

### <span data-ttu-id="711aa-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="711aa-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="711aa-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="711aa-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="711aa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="711aa-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="711aa-108">Lista</span><span class="sxs-lookup"><span data-stu-id="711aa-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="711aa-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="711aa-109">DESCRIPTION</span></span>
<span data-ttu-id="711aa-110">A megadott csatlakoztatott fürt tulajdonságait adja meg, többek között a nevet, identitást, tulajdonságokat és a fürt további részleteit.</span><span class="sxs-lookup"><span data-stu-id="711aa-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="711aa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="711aa-111">EXAMPLES</span></span>

### <span data-ttu-id="711aa-112">Példa 1: az összes csatlakoztatott kubernetes beszerzése az előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="711aa-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="711aa-113">Ez a parancs egy előfizetésben az összes csatlakoztatott kubernetes kapja.</span><span class="sxs-lookup"><span data-stu-id="711aa-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="711aa-114">2. példa: az összes csatlakoztatott kubernetes beolvasása az erőforráscsoport csoportban</span><span class="sxs-lookup"><span data-stu-id="711aa-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="711aa-115">Ez a parancs az összes csatlakoztatott kubernetes bekerül az erőforráscsoport csoportba.</span><span class="sxs-lookup"><span data-stu-id="711aa-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="711aa-116">3. példa: csatlakoztatott kubernetes beszerzése</span><span class="sxs-lookup"><span data-stu-id="711aa-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="711aa-117">Ez a parancs egy csatlakoztatott kubernetes kap.</span><span class="sxs-lookup"><span data-stu-id="711aa-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="711aa-118">Példa 4: kapcsolt kubernetes beszerzése objektum alapján</span><span class="sxs-lookup"><span data-stu-id="711aa-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="711aa-119">Ez a parancs objektummal összekapcsolt kubernetes kap.</span><span class="sxs-lookup"><span data-stu-id="711aa-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="711aa-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="711aa-120">PARAMETERS</span></span>

### <span data-ttu-id="711aa-121">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="711aa-121">-ClusterName</span></span>
<span data-ttu-id="711aa-122">Annak a Kubernetes-csoportnak a neve, amelybe a beszerzést kéri.</span><span class="sxs-lookup"><span data-stu-id="711aa-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="711aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711aa-123">-DefaultProfile</span></span>
<span data-ttu-id="711aa-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="711aa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="711aa-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="711aa-125">-InputObject</span></span>
<span data-ttu-id="711aa-126">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="711aa-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="711aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="711aa-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="711aa-128">The name of the resource group.</span></span>
<span data-ttu-id="711aa-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="711aa-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="711aa-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="711aa-130">-SubscriptionId</span></span>
<span data-ttu-id="711aa-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="711aa-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="711aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711aa-132">CommonParameters</span></span>
<span data-ttu-id="711aa-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="711aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711aa-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="711aa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711aa-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="711aa-135">INPUTS</span></span>

### <span data-ttu-id="711aa-136">Microsoft. Azure. PowerShell. parancsmagok. ConnectedKubernetes. models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="711aa-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="711aa-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="711aa-137">OUTPUTS</span></span>

### <span data-ttu-id="711aa-138">Microsoft. Azure. PowerShell. parancsmagok. ConnectedKubernetes. modellek. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="711aa-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="711aa-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="711aa-139">NOTES</span></span>

<span data-ttu-id="711aa-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="711aa-140">ALIASES</span></span>

<span data-ttu-id="711aa-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="711aa-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="711aa-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="711aa-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="711aa-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="711aa-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="711aa-144">INPUTOBJECT <IConnectedKubernetesIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="711aa-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="711aa-145">`[ClusterName <String>]`: Annak a Kubernetes-csoportnak a neve, amelybe a beszerzést kéri.</span><span class="sxs-lookup"><span data-stu-id="711aa-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="711aa-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="711aa-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="711aa-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="711aa-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="711aa-148">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="711aa-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="711aa-149">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="711aa-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="711aa-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="711aa-150">RELATED LINKS</span></span>

