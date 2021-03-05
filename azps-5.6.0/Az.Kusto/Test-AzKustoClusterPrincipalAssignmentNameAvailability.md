---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f1c96909421dcc21d2b1f318a923ef7f9b804bf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015126"
---
# <span data-ttu-id="2ef1a-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2ef1a-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="2ef1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ef1a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef1a-103">Ellenőrzi, hogy a fő hozzárendelés neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="2ef1a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ef1a-104">SYNTAX</span></span>

### <span data-ttu-id="2ef1a-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ef1a-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2ef1a-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2ef1a-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ef1a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ef1a-107">DESCRIPTION</span></span>
<span data-ttu-id="2ef1a-108">Ellenőrzi, hogy a fő hozzárendelés neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="2ef1a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ef1a-109">EXAMPLES</span></span>

### <span data-ttu-id="2ef1a-110">1. példa: A használt fürt egyszerű hozzárendelési nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="2ef1a-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="2ef1a-111">A fenti parancs azt adja vissza, hogy létezik-e "myprincipal" nevű PrincipalAssignment a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2ef1a-112">2. példa: A nem használt egyszerű hozzárendelési név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="2ef1a-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="2ef1a-113">A fenti parancs azt adja vissza, hogy létezik-e "newprincipal" nevű PrincipalAssignment a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="2ef1a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ef1a-114">PARAMETERS</span></span>

### <span data-ttu-id="2ef1a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2ef1a-115">-ClusterName</span></span>
<span data-ttu-id="2ef1a-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2ef1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef1a-117">-DefaultProfile</span></span>
<span data-ttu-id="2ef1a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ef1a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ef1a-119">-InputObject</span></span>
<span data-ttu-id="2ef1a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ef1a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2ef1a-121">-Name</span></span>
<span data-ttu-id="2ef1a-122">Principal Assignment resource name.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="2ef1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ef1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="2ef1a-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2ef1a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ef1a-125">-SubscriptionId</span></span>
<span data-ttu-id="2ef1a-126">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2ef1a-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2ef1a-128">-Type</span><span class="sxs-lookup"><span data-stu-id="2ef1a-128">-Type</span></span>
<span data-ttu-id="2ef1a-129">Az erőforrás típusa, Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="2ef1a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ef1a-130">-Confirm</span></span>
<span data-ttu-id="2ef1a-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef1a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef1a-132">-WhatIf</span></span>
<span data-ttu-id="2ef1a-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ef1a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef1a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef1a-135">CommonParameters</span></span>
<span data-ttu-id="2ef1a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef1a-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ef1a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef1a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ef1a-138">INPUTS</span></span>

### <span data-ttu-id="2ef1a-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2ef1a-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2ef1a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ef1a-140">OUTPUTS</span></span>

### <span data-ttu-id="2ef1a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="2ef1a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="2ef1a-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ef1a-142">NOTES</span></span>

<span data-ttu-id="2ef1a-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2ef1a-143">ALIASES</span></span>

<span data-ttu-id="2ef1a-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2ef1a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ef1a-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ef1a-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ef1a-147">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2ef1a-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ef1a-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2ef1a-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2ef1a-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2ef1a-151">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2ef1a-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="2ef1a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ef1a-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2ef1a-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2ef1a-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2ef1a-156">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2ef1a-157">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="2ef1a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2ef1a-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ef1a-158">RELATED LINKS</span></span>

