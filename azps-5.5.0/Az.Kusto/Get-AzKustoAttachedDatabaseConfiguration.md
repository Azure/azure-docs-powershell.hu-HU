---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b1a042eb96c1fa6acbcc22fbdd33aefd9d4d46b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152523"
---
# <span data-ttu-id="0d1b2-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d1b2-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="0d1b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1b2-103">Csatolt adatbázis-konfigurációt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="0d1b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0d1b2-104">SYNTAX</span></span>

### <span data-ttu-id="0d1b2-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d1b2-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d1b2-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="0d1b2-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d1b2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d1b2-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d1b2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0d1b2-108">DESCRIPTION</span></span>
<span data-ttu-id="0d1b2-109">Csatolt adatbázis-konfigurációt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="0d1b2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0d1b2-110">EXAMPLES</span></span>

### <span data-ttu-id="0d1b2-111">1. példa: A fürt összes AttachedDatabaseConfigurations tulajdonságának felsorolása</span><span class="sxs-lookup"><span data-stu-id="0d1b2-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="0d1b2-112">A fenti parancs felsorolja a "testnewkustoclusterf" fürt minden AttachedDatabaseConfigurations tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="0d1b2-113">2. példa: Adott AttachedDatabaseConfiguration létrehozása fürtben</span><span class="sxs-lookup"><span data-stu-id="0d1b2-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="0d1b2-114">A fenti parancs a "myfowerconfiguration" AttachedDatabaseConfigurations értéket adja vissza a "testnewkustoclusterf" fürtben.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="0d1b2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d1b2-115">PARAMETERS</span></span>

### <span data-ttu-id="0d1b2-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0d1b2-116">-ClusterName</span></span>
<span data-ttu-id="0d1b2-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0d1b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1b2-118">-DefaultProfile</span></span>
<span data-ttu-id="0d1b2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1b2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d1b2-120">-InputObject</span></span>
<span data-ttu-id="0d1b2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d1b2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0d1b2-122">-Name</span></span>
<span data-ttu-id="0d1b2-123">A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d1b2-125">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0d1b2-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d1b2-126">-SubscriptionId</span></span>
<span data-ttu-id="0d1b2-127">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0d1b2-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0d1b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1b2-129">CommonParameters</span></span>
<span data-ttu-id="0d1b2-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1b2-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d1b2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1b2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d1b2-132">INPUTS</span></span>

### <span data-ttu-id="0d1b2-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0d1b2-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0d1b2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d1b2-134">OUTPUTS</span></span>

### <span data-ttu-id="0d1b2-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.iAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d1b2-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="0d1b2-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0d1b2-136">NOTES</span></span>

<span data-ttu-id="0d1b2-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0d1b2-137">ALIASES</span></span>

<span data-ttu-id="0d1b2-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0d1b2-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d1b2-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d1b2-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d1b2-141">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0d1b2-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d1b2-142">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0d1b2-143">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0d1b2-144">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0d1b2-145">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0d1b2-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0d1b2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d1b2-147">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0d1b2-148">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0d1b2-149">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0d1b2-150">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0d1b2-151">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0d1b2-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d1b2-152">RELATED LINKS</span></span>

