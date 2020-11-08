---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186750"
---
# <span data-ttu-id="9c6e3-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="9c6e3-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="9c6e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c6e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9c6e3-103">API a csatlakoztatott fürterőforrás-erőforrás bizonyos tulajdonságainak frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="9c6e3-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="9c6e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c6e3-104">SYNTAX</span></span>

### <span data-ttu-id="9c6e3-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c6e3-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9c6e3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9c6e3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c6e3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c6e3-107">DESCRIPTION</span></span>
<span data-ttu-id="9c6e3-108">API a csatlakoztatott fürterőforrás-erőforrás bizonyos tulajdonságainak frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="9c6e3-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="9c6e3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9c6e3-109">EXAMPLES</span></span>

### <span data-ttu-id="9c6e3-110">Példa 1: összekapcsolt kubernetes frissítése</span><span class="sxs-lookup"><span data-stu-id="9c6e3-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="9c6e3-111">Ez a parancs frissíti a csatlakoztatott kubernetes.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="9c6e3-112">2. példa: összekapcsolt kubernetes frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="9c6e3-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="9c6e3-113">Ez a parancs az objektum által összekapcsolt kubernetes frissíti.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="9c6e3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c6e3-114">PARAMETERS</span></span>

### <span data-ttu-id="9c6e3-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="9c6e3-115">-ClusterName</span></span>
<span data-ttu-id="9c6e3-116">Annak a Kubernetes-csoportnak a neve, amelybe a beszerzést kéri.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="9c6e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c6e3-117">-DefaultProfile</span></span>
<span data-ttu-id="9c6e3-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c6e3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c6e3-119">-InputObject</span></span>
<span data-ttu-id="9c6e3-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9c6e3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c6e3-121">-ResourceGroupName</span></span>
<span data-ttu-id="9c6e3-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-122">The name of the resource group.</span></span>
<span data-ttu-id="9c6e3-123">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9c6e3-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c6e3-124">-SubscriptionId</span></span>
<span data-ttu-id="9c6e3-125">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9c6e3-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="9c6e3-126">-Tag</span></span>
<span data-ttu-id="9c6e3-127">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-127">Resource tags.</span></span>

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

### <span data-ttu-id="9c6e3-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c6e3-128">-Confirm</span></span>
<span data-ttu-id="9c6e3-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c6e3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c6e3-130">-WhatIf</span></span>
<span data-ttu-id="9c6e3-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c6e3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c6e3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c6e3-133">CommonParameters</span></span>
<span data-ttu-id="9c6e3-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c6e3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c6e3-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c6e3-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c6e3-136">INPUTS</span></span>

### <span data-ttu-id="9c6e3-137">Microsoft. Azure. PowerShell. parancsmagok. ConnectedKubernetes. models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="9c6e3-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="9c6e3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c6e3-138">OUTPUTS</span></span>

### <span data-ttu-id="9c6e3-139">Microsoft. Azure. PowerShell. parancsmagok. ConnectedKubernetes. modellek. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="9c6e3-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="9c6e3-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c6e3-140">NOTES</span></span>

<span data-ttu-id="9c6e3-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9c6e3-141">ALIASES</span></span>

<span data-ttu-id="9c6e3-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="9c6e3-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c6e3-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c6e3-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c6e3-145">INPUTOBJECT <IConnectedKubernetesIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="9c6e3-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c6e3-146">`[ClusterName <String>]`: Annak a Kubernetes-csoportnak a neve, amelybe a beszerzést kéri.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="9c6e3-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9c6e3-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c6e3-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9c6e3-149">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="9c6e3-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9c6e3-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9c6e3-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c6e3-151">RELATED LINKS</span></span>

