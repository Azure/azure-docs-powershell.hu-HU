---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: e1fee17e7f7bf58785c96c28bc6e1f3f66136bb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152475"
---
# <span data-ttu-id="57924-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="57924-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="57924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57924-102">SYNOPSIS</span></span>
<span data-ttu-id="57924-103">Adatkapcsolatot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="57924-103">Returns a data connection.</span></span>

## <span data-ttu-id="57924-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57924-104">SYNTAX</span></span>

### <span data-ttu-id="57924-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57924-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57924-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="57924-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57924-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57924-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="57924-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57924-108">DESCRIPTION</span></span>
<span data-ttu-id="57924-109">Adatkapcsolatot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="57924-109">Returns a data connection.</span></span>

## <span data-ttu-id="57924-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57924-110">EXAMPLES</span></span>

### <span data-ttu-id="57924-111">1. példa: Egy adott adatbázis összes adatkapcsolatának felsorolása</span><span class="sxs-lookup"><span data-stu-id="57924-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="57924-112">A fenti parancs visszaadja a "testrg" erőforráscsoportban található "testnewkustocluster" fürt összes Kusto-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="57924-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="57924-113">2. példa: Adott adatkapcsolat létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="57924-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="57924-114">A fenti parancs a "testrg" erőforráscsoportban található meglévő "testnewkustocluster" "mykustodatabase" nevű adatbázis "mykustodatabase" nevű adatkapcsolatát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="57924-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="57924-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57924-115">PARAMETERS</span></span>

### <span data-ttu-id="57924-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="57924-116">-ClusterName</span></span>
<span data-ttu-id="57924-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="57924-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="57924-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="57924-118">-DatabaseName</span></span>
<span data-ttu-id="57924-119">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="57924-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="57924-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57924-120">-DefaultProfile</span></span>
<span data-ttu-id="57924-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57924-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57924-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57924-122">-InputObject</span></span>
<span data-ttu-id="57924-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="57924-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57924-124">-Name</span><span class="sxs-lookup"><span data-stu-id="57924-124">-Name</span></span>
<span data-ttu-id="57924-125">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="57924-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57924-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57924-126">-ResourceGroupName</span></span>
<span data-ttu-id="57924-127">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="57924-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="57924-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57924-128">-SubscriptionId</span></span>
<span data-ttu-id="57924-129">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="57924-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57924-130">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="57924-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57924-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57924-131">CommonParameters</span></span>
<span data-ttu-id="57924-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57924-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57924-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57924-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57924-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57924-134">INPUTS</span></span>

### <span data-ttu-id="57924-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="57924-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="57924-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57924-136">OUTPUTS</span></span>

### <span data-ttu-id="57924-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="57924-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="57924-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57924-138">NOTES</span></span>

<span data-ttu-id="57924-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="57924-139">ALIASES</span></span>

<span data-ttu-id="57924-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="57924-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57924-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="57924-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57924-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57924-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57924-143">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="57924-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57924-144">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="57924-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="57924-145">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="57924-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="57924-146">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="57924-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="57924-147">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="57924-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="57924-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="57924-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57924-149">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="57924-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="57924-150">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="57924-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="57924-151">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="57924-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="57924-152">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="57924-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="57924-153">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="57924-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="57924-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57924-154">RELATED LINKS</span></span>

