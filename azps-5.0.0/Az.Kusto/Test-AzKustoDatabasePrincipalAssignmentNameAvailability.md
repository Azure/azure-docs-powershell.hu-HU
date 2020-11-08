---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f61bbfc57017f16f9fee0c05f57aa51bd21d364d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187720"
---
# <span data-ttu-id="ab127-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ab127-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="ab127-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab127-102">SYNOPSIS</span></span>
<span data-ttu-id="ab127-103">Ellenőrzi, hogy az adatbázis-fő feladat érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="ab127-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="ab127-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab127-104">SYNTAX</span></span>

### <span data-ttu-id="ab127-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab127-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab127-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ab127-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab127-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab127-107">DESCRIPTION</span></span>
<span data-ttu-id="ab127-108">Ellenőrzi, hogy az adatbázis-fő feladat érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="ab127-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="ab127-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ab127-109">EXAMPLES</span></span>

### <span data-ttu-id="ab127-110">Példa 1: a használatban lévő adatbázis-principalassignment elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="ab127-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="ab127-111">A fenti parancs azt jeleníti meg, hogy a "myprincipal" nevű PrincipalAssignment létezik-e az "mykustodatabase" nevű adatbázis "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ab127-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ab127-112">2. példa: a nem használt adatbázis-principalassignment elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="ab127-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="ab127-113">A fenti parancs azt jeleníti meg, hogy a "myprincipal" nevű PrincipalAssignment létezik-e az "mykustodatabase" nevű adatbázis "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ab127-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="ab127-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab127-114">PARAMETERS</span></span>

### <span data-ttu-id="ab127-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="ab127-115">-ClusterName</span></span>
<span data-ttu-id="ab127-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="ab127-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ab127-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab127-117">-DatabaseName</span></span>
<span data-ttu-id="ab127-118">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="ab127-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ab127-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab127-119">-DefaultProfile</span></span>
<span data-ttu-id="ab127-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab127-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab127-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab127-121">-InputObject</span></span>
<span data-ttu-id="ab127-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ab127-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab127-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab127-123">-Name</span></span>
<span data-ttu-id="ab127-124">Elsődleges hozzárendelés-erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="ab127-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="ab127-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab127-125">-ResourceGroupName</span></span>
<span data-ttu-id="ab127-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ab127-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ab127-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab127-127">-SubscriptionId</span></span>
<span data-ttu-id="ab127-128">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab127-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ab127-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ab127-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ab127-130">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ab127-130">-Type</span></span>
<span data-ttu-id="ab127-131">Az erőforrás típusa, Microsoft. Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="ab127-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="ab127-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab127-132">-Confirm</span></span>
<span data-ttu-id="ab127-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab127-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab127-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab127-134">-WhatIf</span></span>
<span data-ttu-id="ab127-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ab127-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab127-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab127-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab127-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab127-137">CommonParameters</span></span>
<span data-ttu-id="ab127-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab127-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab127-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ab127-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab127-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab127-140">INPUTS</span></span>

### <span data-ttu-id="ab127-141">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ab127-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ab127-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab127-142">OUTPUTS</span></span>

### <span data-ttu-id="ab127-143">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ab127-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="ab127-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab127-144">NOTES</span></span>

<span data-ttu-id="ab127-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ab127-145">ALIASES</span></span>

<span data-ttu-id="ab127-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="ab127-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab127-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ab127-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab127-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ab127-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab127-149">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="ab127-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab127-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="ab127-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ab127-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="ab127-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ab127-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="ab127-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ab127-153">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="ab127-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ab127-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ab127-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab127-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="ab127-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ab127-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="ab127-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ab127-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ab127-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ab127-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab127-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ab127-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ab127-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ab127-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab127-160">RELATED LINKS</span></span>

