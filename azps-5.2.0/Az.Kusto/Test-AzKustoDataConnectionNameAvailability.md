---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371054"
---
# <span data-ttu-id="6aeab-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="6aeab-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="6aeab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aeab-102">SYNOPSIS</span></span>
<span data-ttu-id="6aeab-103">Ellenőrzi, hogy az adatkapcsolat neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="6aeab-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="6aeab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6aeab-104">SYNTAX</span></span>

### <span data-ttu-id="6aeab-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6aeab-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6aeab-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6aeab-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6aeab-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6aeab-107">DESCRIPTION</span></span>
<span data-ttu-id="6aeab-108">Ellenőrzi, hogy az adatkapcsolat neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="6aeab-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="6aeab-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6aeab-109">EXAMPLES</span></span>

### <span data-ttu-id="6aeab-110">1. példa: Adatkapcsolatnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="6aeab-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="6aeab-111">A fenti parancs azt adja vissza, hogy létezik-e "mykustodataconnection" nevű adatkapcsolat a "mykustodatabase" adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="6aeab-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="6aeab-112">2. példa: A nem használt adatkapcsolatnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="6aeab-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="6aeab-113">A fenti parancs azt adja vissza, hogy létezik-e "mydataconnection" nevű adatkapcsolat a "mykustodatabase" adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="6aeab-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="6aeab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6aeab-114">PARAMETERS</span></span>

### <span data-ttu-id="6aeab-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6aeab-115">-ClusterName</span></span>
<span data-ttu-id="6aeab-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeab-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6aeab-117">-DatabaseName</span></span>
<span data-ttu-id="6aeab-118">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-118">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aeab-119">-DefaultProfile</span></span>
<span data-ttu-id="6aeab-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6aeab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aeab-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6aeab-121">-InputObject</span></span>
<span data-ttu-id="6aeab-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6aeab-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aeab-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6aeab-123">-Name</span></span>
<span data-ttu-id="6aeab-124">Adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-124">Data Connection name.</span></span>

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

### <span data-ttu-id="6aeab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aeab-125">-ResourceGroupName</span></span>
<span data-ttu-id="6aeab-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeab-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6aeab-127">-SubscriptionId</span></span>
<span data-ttu-id="6aeab-128">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6aeab-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6aeab-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6aeab-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeab-130">-Type</span><span class="sxs-lookup"><span data-stu-id="6aeab-130">-Type</span></span>
<span data-ttu-id="6aeab-131">Az erőforrás típusa, Microsoft.Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="6aeab-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aeab-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aeab-132">-Confirm</span></span>
<span data-ttu-id="6aeab-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6aeab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aeab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aeab-134">-WhatIf</span></span>
<span data-ttu-id="6aeab-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6aeab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aeab-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6aeab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aeab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aeab-137">CommonParameters</span></span>
<span data-ttu-id="6aeab-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aeab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aeab-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6aeab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aeab-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6aeab-140">INPUTS</span></span>

### <span data-ttu-id="6aeab-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="6aeab-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="6aeab-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6aeab-142">OUTPUTS</span></span>

### <span data-ttu-id="6aeab-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="6aeab-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="6aeab-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6aeab-144">NOTES</span></span>

<span data-ttu-id="6aeab-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6aeab-145">ALIASES</span></span>

<span data-ttu-id="6aeab-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6aeab-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6aeab-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6aeab-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6aeab-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6aeab-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6aeab-149">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6aeab-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6aeab-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="6aeab-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="6aeab-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="6aeab-153">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="6aeab-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6aeab-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6aeab-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="6aeab-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="6aeab-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="6aeab-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6aeab-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="6aeab-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6aeab-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6aeab-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6aeab-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6aeab-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6aeab-160">RELATED LINKS</span></span>

