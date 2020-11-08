---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195883"
---
# <span data-ttu-id="db8fb-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="db8fb-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="db8fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="db8fb-103">Ellenőrzi, hogy az adatkapcsolat neve érvényes-e, és hogy nincs-e már használatban.</span><span class="sxs-lookup"><span data-stu-id="db8fb-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="db8fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db8fb-104">SYNTAX</span></span>

### <span data-ttu-id="db8fb-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db8fb-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db8fb-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="db8fb-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db8fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="db8fb-107">DESCRIPTION</span></span>
<span data-ttu-id="db8fb-108">Ellenőrzi, hogy az adatkapcsolat neve érvényes-e, és hogy nincs-e már használatban.</span><span class="sxs-lookup"><span data-stu-id="db8fb-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="db8fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="db8fb-109">EXAMPLES</span></span>

### <span data-ttu-id="db8fb-110">1. példa: a használatban lévő adatkapcsolati nevek elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="db8fb-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="db8fb-111">A fenti parancs azt jeleníti meg, hogy a "mykustodataconnection" nevű adatkapcsolat létezik-e a "mykustodatabase" adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="db8fb-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="db8fb-112">2. példa: a használatban lévő adatkapcsolati nevek elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="db8fb-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="db8fb-113">A fenti parancs azt jeleníti meg, hogy a "mydataconnection" nevű adatkapcsolat létezik-e a "mykustodatabase" adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="db8fb-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="db8fb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db8fb-114">PARAMETERS</span></span>

### <span data-ttu-id="db8fb-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="db8fb-115">-ClusterName</span></span>
<span data-ttu-id="db8fb-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="db8fb-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="db8fb-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db8fb-117">-DatabaseName</span></span>
<span data-ttu-id="db8fb-118">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="db8fb-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="db8fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db8fb-119">-DefaultProfile</span></span>
<span data-ttu-id="db8fb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db8fb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db8fb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db8fb-121">-InputObject</span></span>
<span data-ttu-id="db8fb-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="db8fb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db8fb-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db8fb-123">-Name</span></span>
<span data-ttu-id="db8fb-124">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="db8fb-124">Data Connection name.</span></span>

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

### <span data-ttu-id="db8fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db8fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="db8fb-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db8fb-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="db8fb-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db8fb-127">-SubscriptionId</span></span>
<span data-ttu-id="db8fb-128">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db8fb-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="db8fb-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="db8fb-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="db8fb-130">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="db8fb-130">-Type</span></span>
<span data-ttu-id="db8fb-131">Az erőforrás típusa, Microsoft. Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="db8fb-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="db8fb-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db8fb-132">-Confirm</span></span>
<span data-ttu-id="db8fb-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db8fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db8fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db8fb-134">-WhatIf</span></span>
<span data-ttu-id="db8fb-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db8fb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db8fb-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db8fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db8fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db8fb-137">CommonParameters</span></span>
<span data-ttu-id="db8fb-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db8fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db8fb-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="db8fb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db8fb-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db8fb-140">INPUTS</span></span>

### <span data-ttu-id="db8fb-141">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="db8fb-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="db8fb-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db8fb-142">OUTPUTS</span></span>

### <span data-ttu-id="db8fb-143">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="db8fb-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="db8fb-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db8fb-144">NOTES</span></span>

<span data-ttu-id="db8fb-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="db8fb-145">ALIASES</span></span>

<span data-ttu-id="db8fb-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="db8fb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db8fb-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="db8fb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db8fb-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="db8fb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db8fb-149">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="db8fb-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db8fb-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="db8fb-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="db8fb-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="db8fb-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="db8fb-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="db8fb-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="db8fb-153">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="db8fb-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="db8fb-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="db8fb-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db8fb-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="db8fb-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="db8fb-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="db8fb-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="db8fb-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db8fb-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="db8fb-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db8fb-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="db8fb-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="db8fb-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="db8fb-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db8fb-160">RELATED LINKS</span></span>

