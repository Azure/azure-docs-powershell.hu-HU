---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184494"
---
# <span data-ttu-id="94da4-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="94da4-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="94da4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94da4-102">SYNOPSIS</span></span>
<span data-ttu-id="94da4-103">Ellenőrzi, hogy a fő hozzárendelés neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="94da4-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="94da4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94da4-104">SYNTAX</span></span>

### <span data-ttu-id="94da4-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94da4-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="94da4-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="94da4-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94da4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="94da4-107">DESCRIPTION</span></span>
<span data-ttu-id="94da4-108">Ellenőrzi, hogy a fő hozzárendelés neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="94da4-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="94da4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="94da4-109">EXAMPLES</span></span>

### <span data-ttu-id="94da4-110">1. példa: a cluster principalassignment-név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="94da4-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="94da4-111">A fenti parancs azt jeleníti meg, hogy a "myprincipal" nevű PrincipalAssignment létezik-e a "testnewkustocluster" nevű fürtben.</span><span class="sxs-lookup"><span data-stu-id="94da4-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="94da4-112">2. példa: a nem használt principalassignment-név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="94da4-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="94da4-113">A fenti parancs azt jeleníti meg, hogy a "newprincipal" nevű PrincipalAssignment létezik-e a "testnewkustocluster" nevű fürtben.</span><span class="sxs-lookup"><span data-stu-id="94da4-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="94da4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94da4-114">PARAMETERS</span></span>

### <span data-ttu-id="94da4-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="94da4-115">-ClusterName</span></span>
<span data-ttu-id="94da4-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="94da4-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94da4-117">-DefaultProfile</span></span>
<span data-ttu-id="94da4-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94da4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94da4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94da4-119">-InputObject</span></span>
<span data-ttu-id="94da4-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94da4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94da4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94da4-121">-Name</span></span>
<span data-ttu-id="94da4-122">Elsődleges hozzárendelés-erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="94da4-122">Principal Assignment resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94da4-123">-ResourceGroupName</span></span>
<span data-ttu-id="94da4-124">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94da4-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94da4-125">-SubscriptionId</span></span>
<span data-ttu-id="94da4-126">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="94da4-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94da4-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94da4-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da4-128">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="94da4-128">-Type</span></span>
<span data-ttu-id="94da4-129">Az erőforrás típusa, Microsoft. Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="94da4-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da4-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94da4-130">-Confirm</span></span>
<span data-ttu-id="94da4-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94da4-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94da4-132">-WhatIf</span></span>
<span data-ttu-id="94da4-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94da4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94da4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94da4-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94da4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94da4-135">CommonParameters</span></span>
<span data-ttu-id="94da4-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94da4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94da4-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94da4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94da4-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94da4-138">INPUTS</span></span>

### <span data-ttu-id="94da4-139">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="94da4-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="94da4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94da4-140">OUTPUTS</span></span>

### <span data-ttu-id="94da4-141">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="94da4-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="94da4-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94da4-142">NOTES</span></span>

<span data-ttu-id="94da4-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="94da4-143">ALIASES</span></span>

<span data-ttu-id="94da4-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="94da4-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94da4-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="94da4-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94da4-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="94da4-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94da4-147">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="94da4-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94da4-148">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="94da4-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="94da4-149">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="94da4-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="94da4-150">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="94da4-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="94da4-151">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="94da4-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="94da4-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="94da4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94da4-153">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="94da4-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="94da4-154">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="94da4-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="94da4-155">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94da4-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="94da4-156">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="94da4-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="94da4-157">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94da4-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94da4-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94da4-158">RELATED LINKS</span></span>

