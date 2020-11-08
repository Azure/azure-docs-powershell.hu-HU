---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186751"
---
# <span data-ttu-id="f5062-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="f5062-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="f5062-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5062-102">SYNOPSIS</span></span>
<span data-ttu-id="f5062-103">Ha törölni kíván egy csatlakoztatott fürtöt, távolítsa el a követett erőforrást az Azure Resource Manager (ARM) alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="f5062-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="f5062-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5062-104">SYNTAX</span></span>

### <span data-ttu-id="f5062-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5062-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f5062-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f5062-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f5062-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5062-107">DESCRIPTION</span></span>
<span data-ttu-id="f5062-108">Ha törölni kíván egy csatlakoztatott fürtöt, távolítsa el a követett erőforrást az Azure Resource Manager (ARM) alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="f5062-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="f5062-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f5062-109">EXAMPLES</span></span>

### <span data-ttu-id="f5062-110">1. példa: csatlakoztatott kubernetes eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5062-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="f5062-111">Ez a parancs eltávolítja a csatlakoztatott kubernetes</span><span class="sxs-lookup"><span data-stu-id="f5062-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="f5062-112">2. példa: összekapcsolt kubernetes objektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5062-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="f5062-113">Ez a parancs eltávolítja az objektum által összekapcsolt kubernetes</span><span class="sxs-lookup"><span data-stu-id="f5062-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="f5062-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5062-114">PARAMETERS</span></span>

### <span data-ttu-id="f5062-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5062-115">-AsJob</span></span>
<span data-ttu-id="f5062-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="f5062-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f5062-117">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="f5062-117">-ClusterName</span></span>
<span data-ttu-id="f5062-118">Annak a Kubernetes-csoportnak a neve, amelybe a beszerzést kéri.</span><span class="sxs-lookup"><span data-stu-id="f5062-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="f5062-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5062-119">-DefaultProfile</span></span>
<span data-ttu-id="f5062-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5062-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5062-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5062-121">-InputObject</span></span>
<span data-ttu-id="f5062-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5062-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f5062-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="f5062-123">-KubeConfig</span></span>
<span data-ttu-id="f5062-124">A Kube konfigurációs fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="f5062-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="f5062-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="f5062-125">-KubeContext</span></span>
<span data-ttu-id="f5062-126">Kubconfig környezet az aktuális számítógépről</span><span class="sxs-lookup"><span data-stu-id="f5062-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="f5062-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="f5062-127">-NoWait</span></span>
<span data-ttu-id="f5062-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="f5062-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f5062-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5062-129">-PassThru</span></span>
<span data-ttu-id="f5062-130">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="f5062-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f5062-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5062-131">-ResourceGroupName</span></span>
<span data-ttu-id="f5062-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5062-132">The name of the resource group.</span></span>
<span data-ttu-id="f5062-133">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f5062-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f5062-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5062-134">-SubscriptionId</span></span>
<span data-ttu-id="f5062-135">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f5062-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f5062-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5062-136">-Confirm</span></span>
<span data-ttu-id="f5062-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5062-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5062-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5062-138">-WhatIf</span></span>
<span data-ttu-id="f5062-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5062-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5062-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5062-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5062-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5062-141">CommonParameters</span></span>
<span data-ttu-id="f5062-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5062-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5062-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5062-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5062-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5062-144">INPUTS</span></span>

### <span data-ttu-id="f5062-145">Microsoft. Azure. PowerShell. parancsmagok. ConnectedKubernetes. models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="f5062-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="f5062-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5062-146">OUTPUTS</span></span>

### <span data-ttu-id="f5062-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5062-147">System.Boolean</span></span>

## <span data-ttu-id="f5062-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5062-148">NOTES</span></span>

<span data-ttu-id="f5062-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f5062-149">ALIASES</span></span>

<span data-ttu-id="f5062-150">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f5062-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5062-151">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f5062-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5062-152">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f5062-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5062-153">INPUTOBJECT <IConnectedKubernetesIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f5062-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5062-154">`[ClusterName <String>]`: Annak a Kubernetes-csoportnak a neve, amelybe a beszerzést kéri.</span><span class="sxs-lookup"><span data-stu-id="f5062-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="f5062-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f5062-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5062-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5062-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f5062-157">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f5062-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="f5062-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f5062-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f5062-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5062-159">RELATED LINKS</span></span>
