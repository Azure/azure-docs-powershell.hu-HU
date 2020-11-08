---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: cdcba65473974da6ba8d526247ca947daa97a55c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181855"
---
# <span data-ttu-id="c0b9e-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="c0b9e-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="c0b9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b9e-103">Egy adatbázis értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-103">Returns a database.</span></span>

## <span data-ttu-id="c0b9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0b9e-104">SYNTAX</span></span>

### <span data-ttu-id="c0b9e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0b9e-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c0b9e-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c0b9e-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c0b9e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c0b9e-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c0b9e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0b9e-108">DESCRIPTION</span></span>
<span data-ttu-id="c0b9e-109">Egy adatbázis értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-109">Returns a database.</span></span>

## <span data-ttu-id="c0b9e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c0b9e-110">EXAMPLES</span></span>

### <span data-ttu-id="c0b9e-111">Példa 1: az összes Kusto-adatbázis listázása egy fürtben név szerint</span><span class="sxs-lookup"><span data-stu-id="c0b9e-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c0b9e-112">A fenti parancs visszaadott minden Kusto-adatbázist a "testnewkustocluster" ("") szektorcsoportban, az "testrg" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c0b9e-113">2. példa: adott Kusto-adatbázis beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="c0b9e-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c0b9e-114">A fenti parancs az "testrg" erőforráscsoport "testnewkustocluster" nevű "mykustodatabase" nevű Kusto-adatbázisát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="c0b9e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0b9e-115">PARAMETERS</span></span>

### <span data-ttu-id="c0b9e-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="c0b9e-116">-ClusterName</span></span>
<span data-ttu-id="c0b9e-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c0b9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b9e-118">-DefaultProfile</span></span>
<span data-ttu-id="c0b9e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0b9e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0b9e-120">-InputObject</span></span>
<span data-ttu-id="c0b9e-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c0b9e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0b9e-122">-Name</span></span>
<span data-ttu-id="c0b9e-123">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0b9e-125">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c0b9e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0b9e-126">-SubscriptionId</span></span>
<span data-ttu-id="c0b9e-127">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c0b9e-128">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c0b9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b9e-129">CommonParameters</span></span>
<span data-ttu-id="c0b9e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0b9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b9e-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b9e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0b9e-132">INPUTS</span></span>

### <span data-ttu-id="c0b9e-133">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c0b9e-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c0b9e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0b9e-134">OUTPUTS</span></span>

### <span data-ttu-id="c0b9e-135">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="c0b9e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="c0b9e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0b9e-136">NOTES</span></span>

<span data-ttu-id="c0b9e-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c0b9e-137">ALIASES</span></span>

<span data-ttu-id="c0b9e-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c0b9e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0b9e-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0b9e-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0b9e-141">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c0b9e-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c0b9e-142">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c0b9e-143">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c0b9e-144">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c0b9e-145">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c0b9e-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c0b9e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0b9e-147">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c0b9e-148">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c0b9e-149">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c0b9e-150">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c0b9e-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c0b9e-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c0b9e-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0b9e-152">RELATED LINKS</span></span>

