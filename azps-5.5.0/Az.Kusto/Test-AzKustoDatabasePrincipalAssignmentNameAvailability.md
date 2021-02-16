---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: b4a670046403aafb4b40740c34f27d7c81bcf8e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203754"
---
# <span data-ttu-id="073b9-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="073b9-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="073b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="073b9-102">SYNOPSIS</span></span>
<span data-ttu-id="073b9-103">Ellenőrzi, hogy az adatbázis-hozzárendelés érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="073b9-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="073b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="073b9-104">SYNTAX</span></span>

### <span data-ttu-id="073b9-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="073b9-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="073b9-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="073b9-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="073b9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="073b9-107">DESCRIPTION</span></span>
<span data-ttu-id="073b9-108">Ellenőrzi, hogy az adatbázis-hozzárendelés érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="073b9-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="073b9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="073b9-109">EXAMPLES</span></span>

### <span data-ttu-id="073b9-110">1. példa: A használatban álló adatbázis-egyszerű hozzárendelési név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="073b9-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="073b9-111">A fenti parancs azt adja vissza, hogy létezik-e "myprincipal" nevű PrincipalAssignment az "mykustodatabase" adatbázisban a "testnewkustocluster" fürtből.</span><span class="sxs-lookup"><span data-stu-id="073b9-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="073b9-112">2. példa: Egy nem használt adatbázis-egyszerű hozzárendelési név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="073b9-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="073b9-113">A fenti parancs azt adja vissza, hogy létezik-e "myprincipal" nevű PrincipalAssignment az "mykustodatabase" adatbázisban a "testnewkustocluster" fürtből.</span><span class="sxs-lookup"><span data-stu-id="073b9-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="073b9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="073b9-114">PARAMETERS</span></span>

### <span data-ttu-id="073b9-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="073b9-115">-ClusterName</span></span>
<span data-ttu-id="073b9-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="073b9-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="073b9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="073b9-117">-DatabaseName</span></span>
<span data-ttu-id="073b9-118">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="073b9-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="073b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073b9-119">-DefaultProfile</span></span>
<span data-ttu-id="073b9-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="073b9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="073b9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="073b9-121">-InputObject</span></span>
<span data-ttu-id="073b9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="073b9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="073b9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="073b9-123">-Name</span></span>
<span data-ttu-id="073b9-124">Principal Assignment resource name.</span><span class="sxs-lookup"><span data-stu-id="073b9-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="073b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="073b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="073b9-126">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="073b9-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="073b9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="073b9-127">-SubscriptionId</span></span>
<span data-ttu-id="073b9-128">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="073b9-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="073b9-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="073b9-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="073b9-130">-Type</span><span class="sxs-lookup"><span data-stu-id="073b9-130">-Type</span></span>
<span data-ttu-id="073b9-131">Az erőforrás típusa, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="073b9-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="073b9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="073b9-132">-Confirm</span></span>
<span data-ttu-id="073b9-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="073b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="073b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="073b9-134">-WhatIf</span></span>
<span data-ttu-id="073b9-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="073b9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="073b9-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="073b9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="073b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073b9-137">CommonParameters</span></span>
<span data-ttu-id="073b9-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="073b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073b9-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="073b9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073b9-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="073b9-140">INPUTS</span></span>

### <span data-ttu-id="073b9-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="073b9-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="073b9-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="073b9-142">OUTPUTS</span></span>

### <span data-ttu-id="073b9-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="073b9-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="073b9-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="073b9-144">NOTES</span></span>

<span data-ttu-id="073b9-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="073b9-145">ALIASES</span></span>

<span data-ttu-id="073b9-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="073b9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="073b9-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="073b9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="073b9-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="073b9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="073b9-149">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="073b9-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="073b9-150">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="073b9-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="073b9-151">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="073b9-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="073b9-152">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="073b9-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="073b9-153">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="073b9-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="073b9-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="073b9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="073b9-155">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="073b9-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="073b9-156">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="073b9-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="073b9-157">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="073b9-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="073b9-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="073b9-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="073b9-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="073b9-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="073b9-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="073b9-160">RELATED LINKS</span></span>

