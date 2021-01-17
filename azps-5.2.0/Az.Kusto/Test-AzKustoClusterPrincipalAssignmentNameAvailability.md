---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350897"
---
# <span data-ttu-id="b1fde-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b1fde-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="b1fde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1fde-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fde-103">Ellenőrzi, hogy a fő hozzárendelés neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="b1fde-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="b1fde-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1fde-104">SYNTAX</span></span>

### <span data-ttu-id="b1fde-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1fde-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b1fde-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b1fde-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1fde-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1fde-107">DESCRIPTION</span></span>
<span data-ttu-id="b1fde-108">Ellenőrzi, hogy a fő hozzárendelés neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="b1fde-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="b1fde-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1fde-109">EXAMPLES</span></span>

### <span data-ttu-id="b1fde-110">1. példa: A használt fürt egyszerű hozzárendelési nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="b1fde-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="b1fde-111">A fenti parancs azt adja vissza, hogy létezik-e "myprincipal" nevű PrincipalAssignment a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="b1fde-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="b1fde-112">2. példa: A nem használt egyszerű hozzárendelési név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="b1fde-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="b1fde-113">A fenti parancs azt adja vissza, hogy létezik-e "newprincipal" nevű PrincipalAssignment a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="b1fde-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="b1fde-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1fde-114">PARAMETERS</span></span>

### <span data-ttu-id="b1fde-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b1fde-115">-ClusterName</span></span>
<span data-ttu-id="b1fde-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b1fde-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b1fde-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fde-117">-DefaultProfile</span></span>
<span data-ttu-id="b1fde-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1fde-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1fde-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1fde-119">-InputObject</span></span>
<span data-ttu-id="b1fde-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b1fde-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1fde-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b1fde-121">-Name</span></span>
<span data-ttu-id="b1fde-122">Principal Assignment resource name.</span><span class="sxs-lookup"><span data-stu-id="b1fde-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="b1fde-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1fde-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1fde-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b1fde-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b1fde-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1fde-125">-SubscriptionId</span></span>
<span data-ttu-id="b1fde-126">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b1fde-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b1fde-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b1fde-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b1fde-128">-Type</span><span class="sxs-lookup"><span data-stu-id="b1fde-128">-Type</span></span>
<span data-ttu-id="b1fde-129">Az erőforrás típusa, Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="b1fde-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="b1fde-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1fde-130">-Confirm</span></span>
<span data-ttu-id="b1fde-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b1fde-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1fde-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1fde-132">-WhatIf</span></span>
<span data-ttu-id="b1fde-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b1fde-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1fde-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1fde-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1fde-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fde-135">CommonParameters</span></span>
<span data-ttu-id="b1fde-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fde-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fde-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1fde-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fde-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1fde-138">INPUTS</span></span>

### <span data-ttu-id="b1fde-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b1fde-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b1fde-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1fde-140">OUTPUTS</span></span>

### <span data-ttu-id="b1fde-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="b1fde-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="b1fde-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1fde-142">NOTES</span></span>

<span data-ttu-id="b1fde-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b1fde-143">ALIASES</span></span>

<span data-ttu-id="b1fde-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b1fde-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1fde-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b1fde-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1fde-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1fde-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1fde-147">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b1fde-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1fde-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="b1fde-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b1fde-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b1fde-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b1fde-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="b1fde-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b1fde-151">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b1fde-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b1fde-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b1fde-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1fde-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="b1fde-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b1fde-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="b1fde-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b1fde-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b1fde-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b1fde-156">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b1fde-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b1fde-157">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b1fde-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b1fde-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1fde-158">RELATED LINKS</span></span>

