---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: b7638780dc4fa360998d7d974d74c93ccd5c2afe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480088"
---
# <span data-ttu-id="71f2e-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="71f2e-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="71f2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="71f2e-103">Frissíti az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="71f2e-103">Updates a database.</span></span>

## <span data-ttu-id="71f2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71f2e-104">SYNTAX</span></span>

### <span data-ttu-id="71f2e-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71f2e-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71f2e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="71f2e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71f2e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71f2e-107">DESCRIPTION</span></span>
<span data-ttu-id="71f2e-108">Frissíti az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="71f2e-108">Updates a database.</span></span>

## <span data-ttu-id="71f2e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71f2e-109">EXAMPLES</span></span>

### <span data-ttu-id="71f2e-110">1. példa: Meglévő adatbázis frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="71f2e-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="71f2e-111">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis "testnewkustocluster" nevű fürtje "testnewkustocluster" nevű, a "testrg" erőforráscsoportban található szoftveres törlési és gyors-gyorsítótár-időszakát.</span><span class="sxs-lookup"><span data-stu-id="71f2e-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="71f2e-112">2. példa: Meglévő adatbázis frissítése identitáson keresztül</span><span class="sxs-lookup"><span data-stu-id="71f2e-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="71f2e-113">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis "testnewkustocluster" nevű fürtje "testnewkustocluster" nevű, a "testrg" erőforráscsoportban található szoftveres törlési és gyors-gyorsítótár-időszakát.</span><span class="sxs-lookup"><span data-stu-id="71f2e-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="71f2e-114">3. példa: Meglévő ReadOnly adatbázis frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="71f2e-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="71f2e-115">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis "mykustodatabase" gyorsgyorsítótár-időszakát a "myfowerwercluster" nevű fürtben, amely a "testrg" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="71f2e-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="71f2e-116">4. példa: Meglévő ReadOnly-adatbázis frissítése identitáson keresztül</span><span class="sxs-lookup"><span data-stu-id="71f2e-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="71f2e-117">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis "mykustodatabase" gyorsgyorsítótár-időszakát a "myfowerwercluster" nevű fürtben, amely a "testrg" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="71f2e-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="71f2e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71f2e-118">PARAMETERS</span></span>

### <span data-ttu-id="71f2e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71f2e-119">-AsJob</span></span>
<span data-ttu-id="71f2e-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="71f2e-120">Run the command as a job</span></span>

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

### <span data-ttu-id="71f2e-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="71f2e-121">-ClusterName</span></span>
<span data-ttu-id="71f2e-122">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="71f2e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f2e-123">-DefaultProfile</span></span>
<span data-ttu-id="71f2e-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71f2e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71f2e-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="71f2e-125">-HotCachePeriod</span></span>
<span data-ttu-id="71f2e-126">A Gyors lekérdezések időkorlában való gyorsítótárazása a TimeSpanban.</span><span class="sxs-lookup"><span data-stu-id="71f2e-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="71f2e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71f2e-127">-InputObject</span></span>
<span data-ttu-id="71f2e-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="71f2e-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71f2e-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="71f2e-129">-Kind</span></span>
<span data-ttu-id="71f2e-130">Az adatbázis fajtája</span><span class="sxs-lookup"><span data-stu-id="71f2e-130">Kind of the database</span></span>

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

### <span data-ttu-id="71f2e-131">-Location</span><span class="sxs-lookup"><span data-stu-id="71f2e-131">-Location</span></span>
<span data-ttu-id="71f2e-132">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="71f2e-132">Resource location.</span></span>

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

### <span data-ttu-id="71f2e-133">-Name</span><span class="sxs-lookup"><span data-stu-id="71f2e-133">-Name</span></span>
<span data-ttu-id="71f2e-134">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="71f2e-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71f2e-135">-NoWait</span></span>
<span data-ttu-id="71f2e-136">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="71f2e-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71f2e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f2e-137">-ResourceGroupName</span></span>
<span data-ttu-id="71f2e-138">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="71f2e-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="71f2e-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="71f2e-140">A TimeSpan lekérdezései számára elérhetővé tétele előtt meg kell tartani az adatokat.</span><span class="sxs-lookup"><span data-stu-id="71f2e-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="71f2e-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71f2e-141">-SubscriptionId</span></span>
<span data-ttu-id="71f2e-142">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="71f2e-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="71f2e-143">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="71f2e-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="71f2e-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71f2e-144">-Confirm</span></span>
<span data-ttu-id="71f2e-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="71f2e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71f2e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71f2e-146">-WhatIf</span></span>
<span data-ttu-id="71f2e-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="71f2e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71f2e-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71f2e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71f2e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f2e-149">CommonParameters</span></span>
<span data-ttu-id="71f2e-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f2e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f2e-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71f2e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f2e-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71f2e-152">INPUTS</span></span>

### <span data-ttu-id="71f2e-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="71f2e-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="71f2e-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71f2e-154">OUTPUTS</span></span>

### <span data-ttu-id="71f2e-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="71f2e-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="71f2e-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71f2e-156">NOTES</span></span>

<span data-ttu-id="71f2e-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="71f2e-157">ALIASES</span></span>

<span data-ttu-id="71f2e-158">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="71f2e-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71f2e-159">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="71f2e-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71f2e-160">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71f2e-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71f2e-161">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="71f2e-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71f2e-162">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="71f2e-163">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="71f2e-164">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="71f2e-165">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="71f2e-166">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="71f2e-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71f2e-167">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="71f2e-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="71f2e-168">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="71f2e-169">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71f2e-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="71f2e-170">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="71f2e-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="71f2e-171">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="71f2e-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="71f2e-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71f2e-172">RELATED LINKS</span></span>

