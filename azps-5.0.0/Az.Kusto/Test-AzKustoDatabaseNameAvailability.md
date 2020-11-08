---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187722"
---
# <span data-ttu-id="40e70-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="40e70-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="40e70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40e70-102">SYNOPSIS</span></span>
<span data-ttu-id="40e70-103">Ellenőrzi, hogy az adatbázis neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="40e70-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="40e70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40e70-104">SYNTAX</span></span>

### <span data-ttu-id="40e70-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40e70-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="40e70-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="40e70-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40e70-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="40e70-107">DESCRIPTION</span></span>
<span data-ttu-id="40e70-108">Ellenőrzi, hogy az adatbázis neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="40e70-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="40e70-109">Példák</span><span class="sxs-lookup"><span data-stu-id="40e70-109">EXAMPLES</span></span>

### <span data-ttu-id="40e70-110">1. példa: Kusto-adatbázis elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="40e70-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="40e70-111">A fenti parancs azt jeleníti meg, hogy a "mykustodatabase" nevű Kusto-adatbázis létezik-e a "testnewkustocluster"-fürtben.</span><span class="sxs-lookup"><span data-stu-id="40e70-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="40e70-112">2. példa: a nem használt Kusto-adatbázis elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="40e70-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="40e70-113">A fenti parancs azt jeleníti meg, hogy a "mykustodatabase2" nevű Kusto-adatbázis létezik-e a "testnewkustocluster"-fürtben.</span><span class="sxs-lookup"><span data-stu-id="40e70-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="40e70-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40e70-114">PARAMETERS</span></span>

### <span data-ttu-id="40e70-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="40e70-115">-ClusterName</span></span>
<span data-ttu-id="40e70-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="40e70-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="40e70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e70-117">-DefaultProfile</span></span>
<span data-ttu-id="40e70-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40e70-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40e70-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40e70-119">-InputObject</span></span>
<span data-ttu-id="40e70-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="40e70-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="40e70-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40e70-121">-Name</span></span>
<span data-ttu-id="40e70-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="40e70-122">Resource name.</span></span>

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

### <span data-ttu-id="40e70-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e70-123">-ResourceGroupName</span></span>
<span data-ttu-id="40e70-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="40e70-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="40e70-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40e70-125">-SubscriptionId</span></span>
<span data-ttu-id="40e70-126">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="40e70-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="40e70-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="40e70-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="40e70-128">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="40e70-128">-Type</span></span>
<span data-ttu-id="40e70-129">Az erőforrás típusa, például: Microsoft. Kusto/Clusters/Databases.</span><span class="sxs-lookup"><span data-stu-id="40e70-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="40e70-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40e70-130">-Confirm</span></span>
<span data-ttu-id="40e70-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40e70-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e70-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e70-132">-WhatIf</span></span>
<span data-ttu-id="40e70-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40e70-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e70-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40e70-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e70-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e70-135">CommonParameters</span></span>
<span data-ttu-id="40e70-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40e70-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e70-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="40e70-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e70-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e70-138">INPUTS</span></span>

### <span data-ttu-id="40e70-139">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="40e70-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="40e70-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e70-140">OUTPUTS</span></span>

### <span data-ttu-id="40e70-141">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="40e70-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="40e70-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40e70-142">NOTES</span></span>

<span data-ttu-id="40e70-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="40e70-143">ALIASES</span></span>

<span data-ttu-id="40e70-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="40e70-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40e70-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="40e70-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40e70-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="40e70-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40e70-147">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="40e70-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40e70-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="40e70-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="40e70-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="40e70-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="40e70-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="40e70-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="40e70-151">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="40e70-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="40e70-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="40e70-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40e70-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="40e70-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="40e70-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="40e70-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="40e70-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="40e70-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="40e70-156">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="40e70-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="40e70-157">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="40e70-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="40e70-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40e70-158">RELATED LINKS</span></span>

