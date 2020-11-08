---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194711"
---
# <span data-ttu-id="204f8-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="204f8-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="204f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="204f8-102">SYNOPSIS</span></span>
<span data-ttu-id="204f8-103">Leválasztja a fürt által birtokolt adatbázis minden híveit.</span><span class="sxs-lookup"><span data-stu-id="204f8-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="204f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="204f8-104">SYNTAX</span></span>

### <span data-ttu-id="204f8-105">DetachExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="204f8-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="204f8-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="204f8-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="204f8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="204f8-107">DESCRIPTION</span></span>
<span data-ttu-id="204f8-108">Leválasztja a fürt által birtokolt adatbázis minden híveit.</span><span class="sxs-lookup"><span data-stu-id="204f8-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="204f8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="204f8-109">EXAMPLES</span></span>

### <span data-ttu-id="204f8-110">1. példa: követő adatbázis leválasztása</span><span class="sxs-lookup"><span data-stu-id="204f8-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="204f8-111">A fenti parancs a "myfollowerconfiguration" AttachedDatabaseConfiguration "" "testnewkustoclusterf"-ról megadott követő adatbázist leválasztja.</span><span class="sxs-lookup"><span data-stu-id="204f8-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="204f8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="204f8-112">PARAMETERS</span></span>

### <span data-ttu-id="204f8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="204f8-113">-AsJob</span></span>
<span data-ttu-id="204f8-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="204f8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="204f8-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="204f8-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="204f8-116">A csatolt adatbázis-konfiguráció erőforrás neve a követő munkacsoportban.</span><span class="sxs-lookup"><span data-stu-id="204f8-116">Resource name of the attached database configuration in the follower cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204f8-117">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="204f8-117">-ClusterName</span></span>
<span data-ttu-id="204f8-118">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="204f8-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204f8-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="204f8-119">-ClusterResourceId</span></span>
<span data-ttu-id="204f8-120">A fürt által birtokolt adatbázist követő fürt erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="204f8-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204f8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204f8-121">-DefaultProfile</span></span>
<span data-ttu-id="204f8-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="204f8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204f8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="204f8-123">-InputObject</span></span>
<span data-ttu-id="204f8-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="204f8-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="204f8-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="204f8-125">-NoWait</span></span>
<span data-ttu-id="204f8-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="204f8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="204f8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="204f8-127">-PassThru</span></span>
<span data-ttu-id="204f8-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="204f8-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="204f8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="204f8-129">-ResourceGroupName</span></span>
<span data-ttu-id="204f8-130">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="204f8-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204f8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="204f8-131">-SubscriptionId</span></span>
<span data-ttu-id="204f8-132">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="204f8-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="204f8-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="204f8-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="204f8-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="204f8-134">-Confirm</span></span>
<span data-ttu-id="204f8-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="204f8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="204f8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="204f8-136">-WhatIf</span></span>
<span data-ttu-id="204f8-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="204f8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="204f8-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="204f8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="204f8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204f8-139">CommonParameters</span></span>
<span data-ttu-id="204f8-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="204f8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204f8-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="204f8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204f8-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="204f8-142">INPUTS</span></span>

### <span data-ttu-id="204f8-143">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="204f8-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="204f8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="204f8-144">OUTPUTS</span></span>

### <span data-ttu-id="204f8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="204f8-145">System.Boolean</span></span>

## <span data-ttu-id="204f8-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="204f8-146">NOTES</span></span>

<span data-ttu-id="204f8-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="204f8-147">ALIASES</span></span>

<span data-ttu-id="204f8-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="204f8-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="204f8-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="204f8-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="204f8-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="204f8-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="204f8-151">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="204f8-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="204f8-152">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="204f8-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="204f8-153">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="204f8-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="204f8-154">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="204f8-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="204f8-155">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="204f8-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="204f8-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="204f8-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="204f8-157">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="204f8-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="204f8-158">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="204f8-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="204f8-159">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="204f8-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="204f8-160">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="204f8-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="204f8-161">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="204f8-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="204f8-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="204f8-162">RELATED LINKS</span></span>

