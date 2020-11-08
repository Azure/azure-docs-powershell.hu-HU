---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184497"
---
# <span data-ttu-id="506bb-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="506bb-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="506bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="506bb-102">SYNOPSIS</span></span>
<span data-ttu-id="506bb-103">Frissít egy adatbázist.</span><span class="sxs-lookup"><span data-stu-id="506bb-103">Updates a database.</span></span>

## <span data-ttu-id="506bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="506bb-104">SYNTAX</span></span>

### <span data-ttu-id="506bb-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="506bb-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="506bb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="506bb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="506bb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="506bb-107">DESCRIPTION</span></span>
<span data-ttu-id="506bb-108">Frissít egy adatbázist.</span><span class="sxs-lookup"><span data-stu-id="506bb-108">Updates a database.</span></span>

## <span data-ttu-id="506bb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="506bb-109">EXAMPLES</span></span>

### <span data-ttu-id="506bb-110">Példa 1: meglévő adatbázis frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="506bb-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="506bb-111">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis Soft törlési időszakát és forró gyorsítótári időszakát a "testrg" erőforráscsoport "testnewkustocluster" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="506bb-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="506bb-112">2. példa: meglévő adatbázis frissítése identitás útján</span><span class="sxs-lookup"><span data-stu-id="506bb-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="506bb-113">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis Soft törlési időszakát és forró gyorsítótári időszakát a "testrg" erőforráscsoport "testnewkustocluster" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="506bb-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="506bb-114">3. példa: létező írásvédett formátumú adatbázis frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="506bb-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="506bb-115">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis forró gyorsítótári időszakát a "myfollowercluster" az erőforráscsoport "testrg" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="506bb-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="506bb-116">4. példa: meglévő ReadOnly-adatbázis frissítése identitás útján</span><span class="sxs-lookup"><span data-stu-id="506bb-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="506bb-117">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis forró gyorsítótári időszakát a "myfollowercluster" az erőforráscsoport "testrg" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="506bb-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="506bb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="506bb-118">PARAMETERS</span></span>

### <span data-ttu-id="506bb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="506bb-119">-AsJob</span></span>
<span data-ttu-id="506bb-120">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="506bb-120">Run the command as a job</span></span>

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

### <span data-ttu-id="506bb-121">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="506bb-121">-ClusterName</span></span>
<span data-ttu-id="506bb-122">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="506bb-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="506bb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506bb-123">-DefaultProfile</span></span>
<span data-ttu-id="506bb-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="506bb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="506bb-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="506bb-125">-HotCachePeriod</span></span>
<span data-ttu-id="506bb-126">Az az időpont, amikor az adatgyorsítótárban meg kell őrizni a gyors lekérdezéseket a időszak-ban.</span><span class="sxs-lookup"><span data-stu-id="506bb-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506bb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="506bb-127">-InputObject</span></span>
<span data-ttu-id="506bb-128">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="506bb-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="506bb-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="506bb-129">-Kind</span></span>
<span data-ttu-id="506bb-130">Az adatbázis típusa</span><span class="sxs-lookup"><span data-stu-id="506bb-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506bb-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="506bb-131">-Location</span></span>
<span data-ttu-id="506bb-132">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="506bb-132">Resource location.</span></span>

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

### <span data-ttu-id="506bb-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="506bb-133">-Name</span></span>
<span data-ttu-id="506bb-134">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="506bb-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506bb-135">-Várva</span><span class="sxs-lookup"><span data-stu-id="506bb-135">-NoWait</span></span>
<span data-ttu-id="506bb-136">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="506bb-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="506bb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506bb-137">-ResourceGroupName</span></span>
<span data-ttu-id="506bb-138">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="506bb-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="506bb-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="506bb-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="506bb-140">Az az időpont, amikor az adatot meg kell őrizni, mielőtt a időszak-ban a lekérdezések elérhetővé válnak.</span><span class="sxs-lookup"><span data-stu-id="506bb-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506bb-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="506bb-141">-SubscriptionId</span></span>
<span data-ttu-id="506bb-142">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="506bb-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="506bb-143">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="506bb-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="506bb-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="506bb-144">-Confirm</span></span>
<span data-ttu-id="506bb-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="506bb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="506bb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="506bb-146">-WhatIf</span></span>
<span data-ttu-id="506bb-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="506bb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="506bb-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="506bb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="506bb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506bb-149">CommonParameters</span></span>
<span data-ttu-id="506bb-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="506bb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506bb-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="506bb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506bb-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="506bb-152">INPUTS</span></span>

### <span data-ttu-id="506bb-153">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="506bb-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="506bb-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="506bb-154">OUTPUTS</span></span>

### <span data-ttu-id="506bb-155">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="506bb-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="506bb-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="506bb-156">NOTES</span></span>

<span data-ttu-id="506bb-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="506bb-157">ALIASES</span></span>

<span data-ttu-id="506bb-158">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="506bb-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="506bb-159">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="506bb-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="506bb-160">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="506bb-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="506bb-161">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="506bb-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="506bb-162">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="506bb-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="506bb-163">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="506bb-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="506bb-164">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="506bb-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="506bb-165">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="506bb-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="506bb-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="506bb-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="506bb-167">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="506bb-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="506bb-168">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="506bb-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="506bb-169">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="506bb-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="506bb-170">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="506bb-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="506bb-171">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="506bb-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="506bb-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="506bb-172">RELATED LINKS</span></span>

