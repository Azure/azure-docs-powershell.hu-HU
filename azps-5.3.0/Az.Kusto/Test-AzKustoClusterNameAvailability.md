---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: d7dc3a154049e486490edddd5fbda52a552d32c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476906"
---
# <span data-ttu-id="6a655-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="6a655-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="6a655-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a655-102">SYNOPSIS</span></span>
<span data-ttu-id="6a655-103">Ellenőrzi, hogy a fürt neve érvényes-e, és még nincs-e használatban.</span><span class="sxs-lookup"><span data-stu-id="6a655-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="6a655-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a655-104">SYNTAX</span></span>

### <span data-ttu-id="6a655-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a655-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a655-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a655-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a655-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a655-107">DESCRIPTION</span></span>
<span data-ttu-id="6a655-108">Ellenőrzi, hogy a fürt neve érvényes-e, és még nincs-e használatban.</span><span class="sxs-lookup"><span data-stu-id="6a655-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="6a655-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a655-109">EXAMPLES</span></span>

### <span data-ttu-id="6a655-110">1. példa: Kusto-fürtnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="6a655-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="6a655-111">A fenti parancs azt adja vissza, hogy létezik-e "testnewkustocluster" nevű Kusto-fürt az "Egyesült Államok keleti részén" vagy sem.</span><span class="sxs-lookup"><span data-stu-id="6a655-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="6a655-112">2. példa: Kusto-fürtnév elérhetőségének ellenőrzése, amely nincs használatban</span><span class="sxs-lookup"><span data-stu-id="6a655-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="6a655-113">A fenti parancs azt adja vissza, hogy az "availablekustocluster" nevű Kusto-fürt létezik-e az "Egyesült Államok keleti részén" vagy sem.</span><span class="sxs-lookup"><span data-stu-id="6a655-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="6a655-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a655-114">PARAMETERS</span></span>

### <span data-ttu-id="6a655-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a655-115">-DefaultProfile</span></span>
<span data-ttu-id="6a655-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a655-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a655-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a655-117">-InputObject</span></span>
<span data-ttu-id="6a655-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6a655-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a655-119">-Location</span><span class="sxs-lookup"><span data-stu-id="6a655-119">-Location</span></span>
<span data-ttu-id="6a655-120">Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="6a655-120">Azure location.</span></span>

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

### <span data-ttu-id="6a655-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6a655-121">-Name</span></span>
<span data-ttu-id="6a655-122">Fürt neve.</span><span class="sxs-lookup"><span data-stu-id="6a655-122">Cluster name.</span></span>

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

### <span data-ttu-id="6a655-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a655-123">-SubscriptionId</span></span>
<span data-ttu-id="6a655-124">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6a655-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a655-125">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6a655-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a655-126">-Type</span><span class="sxs-lookup"><span data-stu-id="6a655-126">-Type</span></span>
<span data-ttu-id="6a655-127">A Microsoft.Kusto/clusters erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="6a655-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="6a655-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a655-128">-Confirm</span></span>
<span data-ttu-id="6a655-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6a655-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a655-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a655-130">-WhatIf</span></span>
<span data-ttu-id="6a655-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6a655-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a655-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a655-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a655-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a655-133">CommonParameters</span></span>
<span data-ttu-id="6a655-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a655-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a655-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a655-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a655-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a655-136">INPUTS</span></span>

### <span data-ttu-id="6a655-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="6a655-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="6a655-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a655-138">OUTPUTS</span></span>

### <span data-ttu-id="6a655-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="6a655-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="6a655-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a655-140">NOTES</span></span>

<span data-ttu-id="6a655-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6a655-141">ALIASES</span></span>

<span data-ttu-id="6a655-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6a655-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a655-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6a655-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a655-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a655-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a655-145">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6a655-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a655-146">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="6a655-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="6a655-147">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="6a655-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="6a655-148">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="6a655-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="6a655-149">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6a655-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="6a655-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6a655-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a655-151">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="6a655-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="6a655-152">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="6a655-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="6a655-153">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6a655-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="6a655-154">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6a655-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6a655-155">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6a655-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6a655-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a655-156">RELATED LINKS</span></span>

