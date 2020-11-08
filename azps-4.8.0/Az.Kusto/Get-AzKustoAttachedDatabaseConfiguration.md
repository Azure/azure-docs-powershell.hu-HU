---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181697"
---
# <span data-ttu-id="c8c29-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c29-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="c8c29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8c29-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c29-103">Egy csatolt adatbázis-konfigurációt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c8c29-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="c8c29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8c29-104">SYNTAX</span></span>

### <span data-ttu-id="c8c29-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8c29-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8c29-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c8c29-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8c29-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8c29-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8c29-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8c29-108">DESCRIPTION</span></span>
<span data-ttu-id="c8c29-109">Egy csatolt adatbázis-konfigurációt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c8c29-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="c8c29-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c8c29-110">EXAMPLES</span></span>

### <span data-ttu-id="c8c29-111">Példa 1: a fürt összes AttachedDatabaseConfigurations listázása</span><span class="sxs-lookup"><span data-stu-id="c8c29-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="c8c29-112">A fenti parancs felsorolja az összes AttachedDatabaseConfigurations a "testnewkustoclusterf" szektorcsoportban.</span><span class="sxs-lookup"><span data-stu-id="c8c29-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="c8c29-113">2. példa: adott AttachedDatabaseConfiguration beszerzése egy fürtben</span><span class="sxs-lookup"><span data-stu-id="c8c29-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="c8c29-114">A fenti parancs a "myfollowerconfiguration" nevű AttachedDatabaseConfigurations a "testnewkustoclusterf" nevű fürtben számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c8c29-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="c8c29-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8c29-115">PARAMETERS</span></span>

### <span data-ttu-id="c8c29-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="c8c29-116">-ClusterName</span></span>
<span data-ttu-id="c8c29-117">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c8c29-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c8c29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c29-118">-DefaultProfile</span></span>
<span data-ttu-id="c8c29-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8c29-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c29-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8c29-120">-InputObject</span></span>
<span data-ttu-id="c8c29-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8c29-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8c29-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8c29-122">-Name</span></span>
<span data-ttu-id="c8c29-123">A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="c8c29-123">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="c8c29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c29-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8c29-125">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c8c29-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c8c29-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8c29-126">-SubscriptionId</span></span>
<span data-ttu-id="c8c29-127">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8c29-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c8c29-128">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c8c29-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c8c29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c29-129">CommonParameters</span></span>
<span data-ttu-id="c8c29-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8c29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c29-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8c29-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c29-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8c29-132">INPUTS</span></span>

### <span data-ttu-id="c8c29-133">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c8c29-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c8c29-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8c29-134">OUTPUTS</span></span>

### <span data-ttu-id="c8c29-135">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c29-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="c8c29-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8c29-136">NOTES</span></span>

<span data-ttu-id="c8c29-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c8c29-137">ALIASES</span></span>

<span data-ttu-id="c8c29-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c8c29-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8c29-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c8c29-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8c29-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c8c29-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8c29-141">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c8c29-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8c29-142">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="c8c29-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c8c29-143">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c8c29-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c8c29-144">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="c8c29-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c8c29-145">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="c8c29-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c8c29-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c8c29-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8c29-147">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="c8c29-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c8c29-148">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="c8c29-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c8c29-149">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c8c29-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c8c29-150">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8c29-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c8c29-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c8c29-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c8c29-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8c29-152">RELATED LINKS</span></span>

