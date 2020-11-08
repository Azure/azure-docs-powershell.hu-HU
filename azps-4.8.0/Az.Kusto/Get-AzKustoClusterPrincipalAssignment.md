---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025678"
---
# <span data-ttu-id="1111e-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="1111e-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="1111e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1111e-102">SYNOPSIS</span></span>
<span data-ttu-id="1111e-103">Kusto-principalAssignment kap.</span><span class="sxs-lookup"><span data-stu-id="1111e-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="1111e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1111e-104">SYNTAX</span></span>

### <span data-ttu-id="1111e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1111e-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1111e-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1111e-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1111e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1111e-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1111e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1111e-108">DESCRIPTION</span></span>
<span data-ttu-id="1111e-109">Kusto-principalAssignment kap.</span><span class="sxs-lookup"><span data-stu-id="1111e-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="1111e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1111e-110">EXAMPLES</span></span>

### <span data-ttu-id="1111e-111">1. példa: az összes Kusto listázása principalAssignment</span><span class="sxs-lookup"><span data-stu-id="1111e-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="1111e-112">A fenti parancs felsorolja az összes principalAssignment a "testnewkustocluster" szektorcsoportban.</span><span class="sxs-lookup"><span data-stu-id="1111e-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="1111e-113">2. példa: Kusto-fürtöt kap principalAssignment név szerint</span><span class="sxs-lookup"><span data-stu-id="1111e-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="1111e-114">A fenti parancs az "testnewkustocluster" nevű fürt "kustoprincipal1" nevű Kusto-principalAssignment jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="1111e-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="1111e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1111e-115">PARAMETERS</span></span>

### <span data-ttu-id="1111e-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="1111e-116">-ClusterName</span></span>
<span data-ttu-id="1111e-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="1111e-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1111e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1111e-118">-DefaultProfile</span></span>
<span data-ttu-id="1111e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1111e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1111e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1111e-120">-InputObject</span></span>
<span data-ttu-id="1111e-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1111e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1111e-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="1111e-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="1111e-123">A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="1111e-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="1111e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1111e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1111e-125">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1111e-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1111e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1111e-126">-SubscriptionId</span></span>
<span data-ttu-id="1111e-127">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1111e-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1111e-128">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1111e-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1111e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1111e-129">CommonParameters</span></span>
<span data-ttu-id="1111e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1111e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1111e-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1111e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1111e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1111e-132">INPUTS</span></span>

### <span data-ttu-id="1111e-133">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1111e-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1111e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1111e-134">OUTPUTS</span></span>

### <span data-ttu-id="1111e-135">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="1111e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="1111e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1111e-136">NOTES</span></span>

<span data-ttu-id="1111e-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1111e-137">ALIASES</span></span>

<span data-ttu-id="1111e-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="1111e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1111e-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1111e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1111e-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1111e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1111e-141">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1111e-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1111e-142">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="1111e-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1111e-143">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="1111e-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1111e-144">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="1111e-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1111e-145">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="1111e-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1111e-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1111e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1111e-147">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="1111e-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1111e-148">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="1111e-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1111e-149">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1111e-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1111e-150">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1111e-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1111e-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1111e-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1111e-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1111e-152">RELATED LINKS</span></span>

