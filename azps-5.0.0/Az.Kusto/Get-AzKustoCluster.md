---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194732"
---
# <span data-ttu-id="a4ec1-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="a4ec1-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="a4ec1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ec1-103">Kusto-fürtöt kap.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="a4ec1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4ec1-104">SYNTAX</span></span>

### <span data-ttu-id="a4ec1-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4ec1-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4ec1-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a4ec1-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4ec1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4ec1-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4ec1-108">Lista</span><span class="sxs-lookup"><span data-stu-id="a4ec1-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ec1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4ec1-109">DESCRIPTION</span></span>
<span data-ttu-id="a4ec1-110">Kusto-fürtöt kap.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="a4ec1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a4ec1-111">EXAMPLES</span></span>

### <span data-ttu-id="a4ec1-112">Példa 1: egy erőforráscsoport összes Kusto listázása</span><span class="sxs-lookup"><span data-stu-id="a4ec1-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="a4ec1-113">A fenti parancs felsorolja az összes Kusto-szektorcsoportot az "testrg" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="a4ec1-114">2. példa: adott Kusto-fürt beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="a4ec1-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="a4ec1-115">A fenti parancs az "testrg" erőforráscsoport "testnewkustocluster" nevű Kusto-fürtöt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="a4ec1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4ec1-116">PARAMETERS</span></span>

### <span data-ttu-id="a4ec1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ec1-117">-DefaultProfile</span></span>
<span data-ttu-id="a4ec1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ec1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4ec1-119">-InputObject</span></span>
<span data-ttu-id="a4ec1-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4ec1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4ec1-121">-Name</span></span>
<span data-ttu-id="a4ec1-122">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a4ec1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ec1-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4ec1-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a4ec1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4ec1-125">-SubscriptionId</span></span>
<span data-ttu-id="a4ec1-126">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a4ec1-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a4ec1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ec1-128">CommonParameters</span></span>
<span data-ttu-id="a4ec1-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4ec1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ec1-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ec1-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ec1-131">INPUTS</span></span>

### <span data-ttu-id="a4ec1-132">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a4ec1-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a4ec1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ec1-133">OUTPUTS</span></span>

### <span data-ttu-id="a4ec1-134">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="a4ec1-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="a4ec1-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4ec1-135">NOTES</span></span>

<span data-ttu-id="a4ec1-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a4ec1-136">ALIASES</span></span>

<span data-ttu-id="a4ec1-137">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a4ec1-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4ec1-138">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4ec1-139">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4ec1-140">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a4ec1-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4ec1-141">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a4ec1-142">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a4ec1-143">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a4ec1-144">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a4ec1-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a4ec1-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4ec1-146">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a4ec1-147">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a4ec1-148">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a4ec1-149">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a4ec1-150">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a4ec1-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a4ec1-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4ec1-151">RELATED LINKS</span></span>

