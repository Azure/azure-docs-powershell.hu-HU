---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194724"
---
# <span data-ttu-id="1f346-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="1f346-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="1f346-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f346-102">SYNOPSIS</span></span>
<span data-ttu-id="1f346-103">Adatkapcsolatot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="1f346-103">Returns a data connection.</span></span>

## <span data-ttu-id="1f346-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f346-104">SYNTAX</span></span>

### <span data-ttu-id="1f346-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f346-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1f346-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1f346-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1f346-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f346-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1f346-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f346-108">DESCRIPTION</span></span>
<span data-ttu-id="1f346-109">Adatkapcsolatot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="1f346-109">Returns a data connection.</span></span>

## <span data-ttu-id="1f346-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1f346-110">EXAMPLES</span></span>

### <span data-ttu-id="1f346-111">Példa 1: adott adatbázis minden adatkapcsolatának listázása</span><span class="sxs-lookup"><span data-stu-id="1f346-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1f346-112">A fenti parancs visszaadott minden Kusto-adatbázist a "testnewkustocluster" ("") szektorcsoportban, az "testrg" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="1f346-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="1f346-113">2. példa: konkrét adatkapcsolat beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="1f346-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1f346-114">A fenti parancs visszaadott "mykustodataconnection" nevű adatkapcsolatot ad eredményül az "mykustodatabase" "testnewkustocluster" nevű "" nevű "" nevű "testrg" erőforráscsoporthoz tartozó "" nevű adatkapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="1f346-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="1f346-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f346-115">PARAMETERS</span></span>

### <span data-ttu-id="1f346-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="1f346-116">-ClusterName</span></span>
<span data-ttu-id="1f346-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="1f346-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1f346-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f346-118">-DatabaseName</span></span>
<span data-ttu-id="1f346-119">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="1f346-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1f346-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f346-120">-DefaultProfile</span></span>
<span data-ttu-id="1f346-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f346-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f346-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f346-122">-InputObject</span></span>
<span data-ttu-id="1f346-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f346-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f346-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f346-124">-Name</span></span>
<span data-ttu-id="1f346-125">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="1f346-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="1f346-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f346-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f346-127">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1f346-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1f346-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f346-128">-SubscriptionId</span></span>
<span data-ttu-id="1f346-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1f346-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1f346-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1f346-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1f346-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f346-131">CommonParameters</span></span>
<span data-ttu-id="1f346-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f346-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f346-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f346-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f346-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f346-134">INPUTS</span></span>

### <span data-ttu-id="1f346-135">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1f346-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1f346-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f346-136">OUTPUTS</span></span>

### <span data-ttu-id="1f346-137">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="1f346-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="1f346-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f346-138">NOTES</span></span>

<span data-ttu-id="1f346-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1f346-139">ALIASES</span></span>

<span data-ttu-id="1f346-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="1f346-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f346-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1f346-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f346-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1f346-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f346-143">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1f346-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f346-144">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="1f346-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1f346-145">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="1f346-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1f346-146">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="1f346-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1f346-147">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="1f346-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1f346-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1f346-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f346-149">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="1f346-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1f346-150">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="1f346-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1f346-151">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1f346-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1f346-152">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1f346-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1f346-153">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1f346-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1f346-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f346-154">RELATED LINKS</span></span>

