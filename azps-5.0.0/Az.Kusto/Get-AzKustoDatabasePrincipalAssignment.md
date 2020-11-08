---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194719"
---
# <span data-ttu-id="c9c85-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c9c85-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="c9c85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9c85-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c85-103">Beolvassa a Kusto-fürt adatbázis-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c9c85-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="c9c85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9c85-104">SYNTAX</span></span>

### <span data-ttu-id="c9c85-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9c85-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9c85-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c9c85-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9c85-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c9c85-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9c85-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9c85-108">DESCRIPTION</span></span>
<span data-ttu-id="c9c85-109">Beolvassa a Kusto-fürt adatbázis-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c9c85-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="c9c85-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c9c85-110">EXAMPLES</span></span>

### <span data-ttu-id="c9c85-111">Példa 1: az adatbázis összes PrincipalAssignment listázása névvel</span><span class="sxs-lookup"><span data-stu-id="c9c85-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="c9c85-112">A fenti parancs visszaadott minden PrincipalAssignment a "mykustodatabase" adatbázisban, amely a "testnewkustocluster" szektorcsoportban található.</span><span class="sxs-lookup"><span data-stu-id="c9c85-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c9c85-113">2. példa: meghatározott PrincipalAssignment beszerzése az adatbázisban név szerint</span><span class="sxs-lookup"><span data-stu-id="c9c85-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="c9c85-114">A fenti parancs visszaadott minden "kustoprincipal1" nevű PrincipalAssignment az "mykustodatabase" nevű adatbázisban, amely a "testnewkustocluster" ("") szektorcsoportban található.</span><span class="sxs-lookup"><span data-stu-id="c9c85-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c9c85-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9c85-115">PARAMETERS</span></span>

### <span data-ttu-id="c9c85-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="c9c85-116">-ClusterName</span></span>
<span data-ttu-id="c9c85-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c9c85-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c9c85-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9c85-118">-DatabaseName</span></span>
<span data-ttu-id="c9c85-119">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="c9c85-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="c9c85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c85-120">-DefaultProfile</span></span>
<span data-ttu-id="c9c85-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9c85-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c85-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9c85-122">-InputObject</span></span>
<span data-ttu-id="c9c85-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9c85-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9c85-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c9c85-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="c9c85-125">A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="c9c85-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="c9c85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c85-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9c85-127">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9c85-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c9c85-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9c85-128">-SubscriptionId</span></span>
<span data-ttu-id="c9c85-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9c85-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c9c85-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c9c85-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c9c85-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c85-131">CommonParameters</span></span>
<span data-ttu-id="c9c85-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9c85-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c85-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9c85-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c85-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c85-134">INPUTS</span></span>

### <span data-ttu-id="c9c85-135">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c9c85-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c9c85-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c85-136">OUTPUTS</span></span>

### <span data-ttu-id="c9c85-137">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c9c85-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="c9c85-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9c85-138">NOTES</span></span>

<span data-ttu-id="c9c85-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c9c85-139">ALIASES</span></span>

<span data-ttu-id="c9c85-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c9c85-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9c85-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c9c85-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9c85-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c9c85-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9c85-143">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c9c85-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9c85-144">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="c9c85-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c9c85-145">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c9c85-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c9c85-146">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="c9c85-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c9c85-147">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="c9c85-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c9c85-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c9c85-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9c85-149">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="c9c85-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c9c85-150">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="c9c85-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c9c85-151">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9c85-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c9c85-152">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9c85-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c9c85-153">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c9c85-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c9c85-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9c85-154">RELATED LINKS</span></span>

