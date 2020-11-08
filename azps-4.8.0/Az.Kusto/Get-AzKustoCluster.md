---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181698"
---
# <span data-ttu-id="aa56d-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="aa56d-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="aa56d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa56d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa56d-103">Kusto-fürtöt kap.</span><span class="sxs-lookup"><span data-stu-id="aa56d-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="aa56d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa56d-104">SYNTAX</span></span>

### <span data-ttu-id="aa56d-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa56d-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aa56d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="aa56d-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aa56d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa56d-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aa56d-108">Lista</span><span class="sxs-lookup"><span data-stu-id="aa56d-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa56d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa56d-109">DESCRIPTION</span></span>
<span data-ttu-id="aa56d-110">Kusto-fürtöt kap.</span><span class="sxs-lookup"><span data-stu-id="aa56d-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="aa56d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="aa56d-111">EXAMPLES</span></span>

### <span data-ttu-id="aa56d-112">Példa 1: egy erőforráscsoport összes Kusto listázása</span><span class="sxs-lookup"><span data-stu-id="aa56d-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="aa56d-113">A fenti parancs felsorolja az összes Kusto-szektorcsoportot az "testrg" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="aa56d-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="aa56d-114">2. példa: adott Kusto-fürt beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="aa56d-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="aa56d-115">A fenti parancs az "testrg" erőforráscsoport "testnewkustocluster" nevű Kusto-fürtöt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="aa56d-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="aa56d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa56d-116">PARAMETERS</span></span>

### <span data-ttu-id="aa56d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa56d-117">-DefaultProfile</span></span>
<span data-ttu-id="aa56d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa56d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa56d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa56d-119">-InputObject</span></span>
<span data-ttu-id="aa56d-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa56d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa56d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa56d-121">-Name</span></span>
<span data-ttu-id="aa56d-122">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="aa56d-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="aa56d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa56d-123">-ResourceGroupName</span></span>
<span data-ttu-id="aa56d-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aa56d-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="aa56d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa56d-125">-SubscriptionId</span></span>
<span data-ttu-id="aa56d-126">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa56d-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aa56d-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="aa56d-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aa56d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa56d-128">CommonParameters</span></span>
<span data-ttu-id="aa56d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa56d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa56d-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa56d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa56d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa56d-131">INPUTS</span></span>

### <span data-ttu-id="aa56d-132">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="aa56d-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="aa56d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa56d-133">OUTPUTS</span></span>

### <span data-ttu-id="aa56d-134">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="aa56d-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="aa56d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa56d-135">NOTES</span></span>

<span data-ttu-id="aa56d-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aa56d-136">ALIASES</span></span>

<span data-ttu-id="aa56d-137">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="aa56d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa56d-138">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="aa56d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa56d-139">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="aa56d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa56d-140">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="aa56d-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa56d-141">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="aa56d-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="aa56d-142">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="aa56d-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="aa56d-143">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="aa56d-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="aa56d-144">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="aa56d-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="aa56d-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="aa56d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa56d-146">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="aa56d-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="aa56d-147">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="aa56d-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="aa56d-148">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aa56d-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="aa56d-149">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa56d-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aa56d-150">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="aa56d-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="aa56d-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa56d-151">RELATED LINKS</span></span>

