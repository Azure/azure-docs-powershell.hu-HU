---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194727"
---
# <span data-ttu-id="c6efc-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c6efc-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="c6efc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6efc-102">SYNOPSIS</span></span>
<span data-ttu-id="c6efc-103">Kusto-principalAssignment kap.</span><span class="sxs-lookup"><span data-stu-id="c6efc-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="c6efc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6efc-104">SYNTAX</span></span>

### <span data-ttu-id="c6efc-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6efc-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6efc-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c6efc-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6efc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6efc-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6efc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6efc-108">DESCRIPTION</span></span>
<span data-ttu-id="c6efc-109">Kusto-principalAssignment kap.</span><span class="sxs-lookup"><span data-stu-id="c6efc-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="c6efc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c6efc-110">EXAMPLES</span></span>

### <span data-ttu-id="c6efc-111">1. példa: az összes Kusto listázása principalAssignment</span><span class="sxs-lookup"><span data-stu-id="c6efc-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="c6efc-112">A fenti parancs felsorolja az összes principalAssignment a "testnewkustocluster" szektorcsoportban.</span><span class="sxs-lookup"><span data-stu-id="c6efc-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c6efc-113">2. példa: Kusto-fürtöt kap principalAssignment név szerint</span><span class="sxs-lookup"><span data-stu-id="c6efc-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="c6efc-114">A fenti parancs az "testnewkustocluster" nevű fürt "kustoprincipal1" nevű Kusto-principalAssignment jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="c6efc-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c6efc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6efc-115">PARAMETERS</span></span>

### <span data-ttu-id="c6efc-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="c6efc-116">-ClusterName</span></span>
<span data-ttu-id="c6efc-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c6efc-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c6efc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6efc-118">-DefaultProfile</span></span>
<span data-ttu-id="c6efc-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6efc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6efc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6efc-120">-InputObject</span></span>
<span data-ttu-id="c6efc-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6efc-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c6efc-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c6efc-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="c6efc-123">A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="c6efc-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="c6efc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6efc-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6efc-125">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6efc-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c6efc-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6efc-126">-SubscriptionId</span></span>
<span data-ttu-id="c6efc-127">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c6efc-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c6efc-128">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c6efc-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c6efc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6efc-129">CommonParameters</span></span>
<span data-ttu-id="c6efc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6efc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6efc-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6efc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6efc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6efc-132">INPUTS</span></span>

### <span data-ttu-id="c6efc-133">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c6efc-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c6efc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6efc-134">OUTPUTS</span></span>

### <span data-ttu-id="c6efc-135">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c6efc-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="c6efc-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6efc-136">NOTES</span></span>

<span data-ttu-id="c6efc-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c6efc-137">ALIASES</span></span>

<span data-ttu-id="c6efc-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c6efc-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6efc-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c6efc-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6efc-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c6efc-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6efc-141">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c6efc-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6efc-142">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="c6efc-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c6efc-143">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c6efc-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c6efc-144">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="c6efc-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c6efc-145">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="c6efc-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c6efc-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c6efc-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6efc-147">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="c6efc-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c6efc-148">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="c6efc-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c6efc-149">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6efc-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c6efc-150">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c6efc-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c6efc-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c6efc-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c6efc-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6efc-152">RELATED LINKS</span></span>

