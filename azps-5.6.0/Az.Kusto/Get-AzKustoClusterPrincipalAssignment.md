---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b89327f80ec5f8e0f5faf9f66e943ee07601799e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924857"
---
# <span data-ttu-id="20930-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="20930-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="20930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20930-102">SYNOPSIS</span></span>
<span data-ttu-id="20930-103">Kusto-fürt egyszerű hozzárendelését kapja.</span><span class="sxs-lookup"><span data-stu-id="20930-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="20930-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20930-104">SYNTAX</span></span>

### <span data-ttu-id="20930-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20930-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="20930-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="20930-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="20930-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20930-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="20930-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20930-108">DESCRIPTION</span></span>
<span data-ttu-id="20930-109">Kusto-fürt egyszerű hozzárendelését kapja.</span><span class="sxs-lookup"><span data-stu-id="20930-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="20930-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20930-110">EXAMPLES</span></span>

### <span data-ttu-id="20930-111">1. példa: Az összes Kusto-fürt egyszerű hozzárendelésének felsorolása</span><span class="sxs-lookup"><span data-stu-id="20930-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="20930-112">A fenti parancs felsorolja a "testnewkustocluster" fürt összes egyszerű Hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="20930-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="20930-113">2. példa: Kusto-fürt egyszerű hozzárendelése név szerint</span><span class="sxs-lookup"><span data-stu-id="20930-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="20930-114">A fenti parancs a Kusto cluster principalAssignment (kustoprincipal1) nevet adja vissza a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="20930-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="20930-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20930-115">PARAMETERS</span></span>

### <span data-ttu-id="20930-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="20930-116">-ClusterName</span></span>
<span data-ttu-id="20930-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="20930-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20930-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20930-118">-DefaultProfile</span></span>
<span data-ttu-id="20930-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20930-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20930-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20930-120">-InputObject</span></span>
<span data-ttu-id="20930-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="20930-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20930-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="20930-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="20930-123">A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="20930-123">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20930-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20930-124">-ResourceGroupName</span></span>
<span data-ttu-id="20930-125">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="20930-125">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20930-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20930-126">-SubscriptionId</span></span>
<span data-ttu-id="20930-127">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="20930-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="20930-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="20930-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20930-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20930-129">CommonParameters</span></span>
<span data-ttu-id="20930-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20930-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20930-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20930-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20930-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20930-132">INPUTS</span></span>

### <span data-ttu-id="20930-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="20930-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="20930-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20930-134">OUTPUTS</span></span>

### <span data-ttu-id="20930-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="20930-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="20930-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20930-136">NOTES</span></span>

<span data-ttu-id="20930-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="20930-137">ALIASES</span></span>

<span data-ttu-id="20930-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="20930-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20930-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="20930-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20930-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20930-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20930-141">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="20930-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20930-142">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="20930-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="20930-143">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="20930-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="20930-144">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="20930-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="20930-145">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="20930-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="20930-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="20930-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20930-147">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="20930-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="20930-148">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="20930-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="20930-149">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="20930-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="20930-150">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="20930-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="20930-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="20930-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="20930-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20930-152">RELATED LINKS</span></span>

