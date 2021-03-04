---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 753f2e4f2a1e2b60a12570307b518a5f2a78887b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924882"
---
# <span data-ttu-id="90643-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="90643-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="90643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90643-102">SYNOPSIS</span></span>
<span data-ttu-id="90643-103">Kusto-fürtöt kap.</span><span class="sxs-lookup"><span data-stu-id="90643-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="90643-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90643-104">SYNTAX</span></span>

### <span data-ttu-id="90643-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90643-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="90643-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="90643-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="90643-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90643-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="90643-108">Lista</span><span class="sxs-lookup"><span data-stu-id="90643-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="90643-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90643-109">DESCRIPTION</span></span>
<span data-ttu-id="90643-110">Kusto-fürtöt kap.</span><span class="sxs-lookup"><span data-stu-id="90643-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="90643-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90643-111">EXAMPLES</span></span>

### <span data-ttu-id="90643-112">1. példa: Egy erőforráscsoport összes Kusto-fürtének felsorolása</span><span class="sxs-lookup"><span data-stu-id="90643-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="90643-113">A fenti parancs felsorolja a "testrg" erőforráscsoport összes Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="90643-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="90643-114">2. példa: Adott Kusto-fürt lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="90643-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="90643-115">A fenti parancs a "testrg" erőforráscsoportban a "testnewkustocluster" nevű Kusto-fürtöt adja vissza.</span><span class="sxs-lookup"><span data-stu-id="90643-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="90643-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90643-116">PARAMETERS</span></span>

### <span data-ttu-id="90643-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90643-117">-DefaultProfile</span></span>
<span data-ttu-id="90643-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90643-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90643-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90643-119">-InputObject</span></span>
<span data-ttu-id="90643-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="90643-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90643-121">-Name</span><span class="sxs-lookup"><span data-stu-id="90643-121">-Name</span></span>
<span data-ttu-id="90643-122">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="90643-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90643-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90643-123">-ResourceGroupName</span></span>
<span data-ttu-id="90643-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="90643-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="90643-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90643-125">-SubscriptionId</span></span>
<span data-ttu-id="90643-126">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="90643-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="90643-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="90643-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90643-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90643-128">CommonParameters</span></span>
<span data-ttu-id="90643-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90643-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90643-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90643-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90643-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90643-131">INPUTS</span></span>

### <span data-ttu-id="90643-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="90643-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="90643-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90643-133">OUTPUTS</span></span>

### <span data-ttu-id="90643-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="90643-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="90643-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90643-135">NOTES</span></span>

<span data-ttu-id="90643-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="90643-136">ALIASES</span></span>

<span data-ttu-id="90643-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="90643-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90643-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="90643-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90643-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90643-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90643-140">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="90643-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90643-141">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="90643-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="90643-142">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="90643-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="90643-143">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="90643-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="90643-144">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="90643-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="90643-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="90643-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90643-146">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="90643-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="90643-147">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="90643-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="90643-148">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="90643-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="90643-149">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="90643-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="90643-150">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="90643-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="90643-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90643-151">RELATED LINKS</span></span>

