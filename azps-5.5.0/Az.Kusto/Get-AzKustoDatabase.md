---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152467"
---
# <span data-ttu-id="76c40-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="76c40-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="76c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c40-102">SYNOPSIS</span></span>
<span data-ttu-id="76c40-103">Adatbázist ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="76c40-103">Returns a database.</span></span>

## <span data-ttu-id="76c40-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="76c40-104">SYNTAX</span></span>

### <span data-ttu-id="76c40-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76c40-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76c40-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="76c40-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76c40-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76c40-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="76c40-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="76c40-108">DESCRIPTION</span></span>
<span data-ttu-id="76c40-109">Adatbázist ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="76c40-109">Returns a database.</span></span>

## <span data-ttu-id="76c40-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="76c40-110">EXAMPLES</span></span>

### <span data-ttu-id="76c40-111">1. példa: Egy fürt összes Kusto-adatbázisának felsorolása név szerint</span><span class="sxs-lookup"><span data-stu-id="76c40-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="76c40-112">A fenti parancs visszaadja a "testrg" erőforráscsoportban található "testnewkustocluster" fürt összes Kusto-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="76c40-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="76c40-113">2. példa: Adott Kusto-adatbázis lekért neve</span><span class="sxs-lookup"><span data-stu-id="76c40-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="76c40-114">A fenti parancs visszaadja a "testrg" erőforráscsoportban található "testnewkustocluster" fürt "mykustodatabase" nevű Kusto-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="76c40-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="76c40-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76c40-115">PARAMETERS</span></span>

### <span data-ttu-id="76c40-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="76c40-116">-ClusterName</span></span>
<span data-ttu-id="76c40-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="76c40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c40-118">-DefaultProfile</span></span>
<span data-ttu-id="76c40-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76c40-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c40-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76c40-120">-InputObject</span></span>
<span data-ttu-id="76c40-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="76c40-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76c40-122">-Name</span><span class="sxs-lookup"><span data-stu-id="76c40-122">-Name</span></span>
<span data-ttu-id="76c40-123">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="76c40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c40-124">-ResourceGroupName</span></span>
<span data-ttu-id="76c40-125">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="76c40-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76c40-126">-SubscriptionId</span></span>
<span data-ttu-id="76c40-127">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="76c40-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76c40-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="76c40-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="76c40-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c40-129">CommonParameters</span></span>
<span data-ttu-id="76c40-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c40-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c40-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76c40-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c40-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76c40-132">INPUTS</span></span>

### <span data-ttu-id="76c40-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="76c40-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="76c40-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76c40-134">OUTPUTS</span></span>

### <span data-ttu-id="76c40-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="76c40-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="76c40-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="76c40-136">NOTES</span></span>

<span data-ttu-id="76c40-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="76c40-137">ALIASES</span></span>

<span data-ttu-id="76c40-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="76c40-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76c40-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="76c40-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76c40-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76c40-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76c40-141">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="76c40-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76c40-142">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="76c40-143">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="76c40-144">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="76c40-145">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="76c40-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="76c40-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76c40-147">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="76c40-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="76c40-148">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="76c40-149">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="76c40-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="76c40-150">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="76c40-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="76c40-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="76c40-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="76c40-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76c40-152">RELATED LINKS</span></span>

