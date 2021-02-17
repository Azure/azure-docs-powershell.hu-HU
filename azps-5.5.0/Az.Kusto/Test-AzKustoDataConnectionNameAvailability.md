---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 14eee624f4de3129ddeefee05d402abb0cb686db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147658"
---
# <span data-ttu-id="f4493-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f4493-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="f4493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4493-102">SYNOPSIS</span></span>
<span data-ttu-id="f4493-103">Ellenőrzi, hogy az adatkapcsolat neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="f4493-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="f4493-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4493-104">SYNTAX</span></span>

### <span data-ttu-id="f4493-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4493-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f4493-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f4493-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f4493-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4493-107">DESCRIPTION</span></span>
<span data-ttu-id="f4493-108">Ellenőrzi, hogy az adatkapcsolat neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="f4493-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="f4493-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4493-109">EXAMPLES</span></span>

### <span data-ttu-id="f4493-110">1. példa: Adatkapcsolatnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="f4493-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="f4493-111">A fenti parancs azt adja vissza, hogy létezik-e "mykustodataconnection" nevű adatkapcsolat a "mykustodatabase" adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="f4493-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="f4493-112">2. példa: A nem használt adatkapcsolatnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="f4493-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="f4493-113">A fenti parancs azt adja vissza, hogy létezik-e "mydataconnection" nevű adatkapcsolat a "mykustodatabase" adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="f4493-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="f4493-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4493-114">PARAMETERS</span></span>

### <span data-ttu-id="f4493-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f4493-115">-ClusterName</span></span>
<span data-ttu-id="f4493-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f4493-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4493-117">-DatabaseName</span></span>
<span data-ttu-id="f4493-118">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f4493-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4493-119">-DefaultProfile</span></span>
<span data-ttu-id="f4493-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4493-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4493-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4493-121">-InputObject</span></span>
<span data-ttu-id="f4493-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f4493-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4493-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f4493-123">-Name</span></span>
<span data-ttu-id="f4493-124">Adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-124">Data Connection name.</span></span>

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

### <span data-ttu-id="f4493-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4493-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4493-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f4493-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4493-127">-SubscriptionId</span></span>
<span data-ttu-id="f4493-128">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f4493-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f4493-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f4493-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f4493-130">-Type</span><span class="sxs-lookup"><span data-stu-id="f4493-130">-Type</span></span>
<span data-ttu-id="f4493-131">Az erőforrás típusa, Microsoft.Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="f4493-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="f4493-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4493-132">-Confirm</span></span>
<span data-ttu-id="f4493-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f4493-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4493-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4493-134">-WhatIf</span></span>
<span data-ttu-id="f4493-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f4493-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4493-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4493-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4493-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4493-137">CommonParameters</span></span>
<span data-ttu-id="f4493-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4493-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4493-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4493-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4493-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4493-140">INPUTS</span></span>

### <span data-ttu-id="f4493-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f4493-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f4493-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4493-142">OUTPUTS</span></span>

### <span data-ttu-id="f4493-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="f4493-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="f4493-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4493-144">NOTES</span></span>

<span data-ttu-id="f4493-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f4493-145">ALIASES</span></span>

<span data-ttu-id="f4493-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f4493-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4493-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f4493-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4493-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4493-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4493-149">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f4493-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4493-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f4493-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f4493-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f4493-153">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f4493-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f4493-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4493-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="f4493-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f4493-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="f4493-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f4493-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4493-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f4493-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f4493-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f4493-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f4493-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f4493-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4493-160">RELATED LINKS</span></span>

