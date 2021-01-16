---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349229"
---
# <span data-ttu-id="57bad-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="57bad-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="57bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57bad-102">SYNOPSIS</span></span>
<span data-ttu-id="57bad-103">Kusto-fürtadatbázis-hozzárendelést kap.</span><span class="sxs-lookup"><span data-stu-id="57bad-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="57bad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57bad-104">SYNTAX</span></span>

### <span data-ttu-id="57bad-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57bad-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57bad-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="57bad-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57bad-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57bad-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="57bad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57bad-108">DESCRIPTION</span></span>
<span data-ttu-id="57bad-109">Kusto-fürtadatbázis-hozzárendelést kap.</span><span class="sxs-lookup"><span data-stu-id="57bad-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="57bad-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57bad-110">EXAMPLES</span></span>

### <span data-ttu-id="57bad-111">1. példa: Adatbázis összes PrincipalAssignment-hozzárendelésének felsorolása név szerint</span><span class="sxs-lookup"><span data-stu-id="57bad-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="57bad-112">A fenti parancs az adatbázis "mykustodatabase" összes PrincipalAssignment-ét visszaadja, amely a "testnewkustocluster" fürtben található.</span><span class="sxs-lookup"><span data-stu-id="57bad-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="57bad-113">2. példa: Adott PrincipalAssignment lekérdezése egy adatbázisban név szerint</span><span class="sxs-lookup"><span data-stu-id="57bad-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="57bad-114">A fenti parancs visszaadja a "testnewkustocluster" fürtben található "mykustodatabase" adatbázisban található összes "kustoprincipal1" nevű PrincipalAssignment-et.</span><span class="sxs-lookup"><span data-stu-id="57bad-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="57bad-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57bad-115">PARAMETERS</span></span>

### <span data-ttu-id="57bad-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="57bad-116">-ClusterName</span></span>
<span data-ttu-id="57bad-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="57bad-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="57bad-118">-DatabaseName</span></span>
<span data-ttu-id="57bad-119">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="57bad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57bad-120">-DefaultProfile</span></span>
<span data-ttu-id="57bad-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57bad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57bad-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57bad-122">-InputObject</span></span>
<span data-ttu-id="57bad-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="57bad-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57bad-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="57bad-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="57bad-125">A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="57bad-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="57bad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57bad-126">-ResourceGroupName</span></span>
<span data-ttu-id="57bad-127">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="57bad-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57bad-128">-SubscriptionId</span></span>
<span data-ttu-id="57bad-129">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="57bad-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57bad-130">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="57bad-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57bad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57bad-131">CommonParameters</span></span>
<span data-ttu-id="57bad-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57bad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57bad-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57bad-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57bad-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57bad-134">INPUTS</span></span>

### <span data-ttu-id="57bad-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="57bad-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="57bad-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57bad-136">OUTPUTS</span></span>

### <span data-ttu-id="57bad-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="57bad-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="57bad-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57bad-138">NOTES</span></span>

<span data-ttu-id="57bad-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="57bad-139">ALIASES</span></span>

<span data-ttu-id="57bad-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="57bad-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57bad-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="57bad-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57bad-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57bad-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57bad-143">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="57bad-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57bad-144">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="57bad-145">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="57bad-146">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="57bad-147">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="57bad-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="57bad-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57bad-149">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="57bad-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="57bad-150">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="57bad-151">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="57bad-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="57bad-152">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="57bad-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="57bad-153">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="57bad-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="57bad-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57bad-154">RELATED LINKS</span></span>

