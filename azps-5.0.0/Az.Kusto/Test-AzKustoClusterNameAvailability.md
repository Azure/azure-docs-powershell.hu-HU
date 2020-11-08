---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195890"
---
# <span data-ttu-id="29dfb-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="29dfb-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="29dfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="29dfb-103">Ellenőrzi, hogy a fürt neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="29dfb-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="29dfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29dfb-104">SYNTAX</span></span>

### <span data-ttu-id="29dfb-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29dfb-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="29dfb-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="29dfb-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29dfb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29dfb-107">DESCRIPTION</span></span>
<span data-ttu-id="29dfb-108">Ellenőrzi, hogy a fürt neve érvényes-e, és még nincs használatban.</span><span class="sxs-lookup"><span data-stu-id="29dfb-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="29dfb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29dfb-109">EXAMPLES</span></span>

### <span data-ttu-id="29dfb-110">1. példa: Kusto-fürt elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="29dfb-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="29dfb-111">A fenti parancs azt jeleníti meg, hogy a "testnewkustocluster" nevű Kusto-fürt létezik-e a "Kelet-amerikai" régióban.</span><span class="sxs-lookup"><span data-stu-id="29dfb-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="29dfb-112">2. példa: a Kusto-fürtök elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="29dfb-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="29dfb-113">A fenti parancs azt jeleníti meg, hogy a "availablekustocluster" nevű Kusto-fürt létezik-e a "Kelet-amerikai" régióban.</span><span class="sxs-lookup"><span data-stu-id="29dfb-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="29dfb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29dfb-114">PARAMETERS</span></span>

### <span data-ttu-id="29dfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dfb-115">-DefaultProfile</span></span>
<span data-ttu-id="29dfb-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29dfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29dfb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29dfb-117">-InputObject</span></span>
<span data-ttu-id="29dfb-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="29dfb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="29dfb-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="29dfb-119">-Location</span></span>
<span data-ttu-id="29dfb-120">Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="29dfb-120">Azure location.</span></span>

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

### <span data-ttu-id="29dfb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29dfb-121">-Name</span></span>
<span data-ttu-id="29dfb-122">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="29dfb-122">Cluster name.</span></span>

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

### <span data-ttu-id="29dfb-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29dfb-123">-SubscriptionId</span></span>
<span data-ttu-id="29dfb-124">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29dfb-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="29dfb-125">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="29dfb-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="29dfb-126">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="29dfb-126">-Type</span></span>
<span data-ttu-id="29dfb-127">Az erőforrás típusa, Microsoft. Kusto/klaszterek.</span><span class="sxs-lookup"><span data-stu-id="29dfb-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="29dfb-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29dfb-128">-Confirm</span></span>
<span data-ttu-id="29dfb-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29dfb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29dfb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29dfb-130">-WhatIf</span></span>
<span data-ttu-id="29dfb-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29dfb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29dfb-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29dfb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29dfb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dfb-133">CommonParameters</span></span>
<span data-ttu-id="29dfb-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29dfb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dfb-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="29dfb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dfb-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29dfb-136">INPUTS</span></span>

### <span data-ttu-id="29dfb-137">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="29dfb-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="29dfb-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29dfb-138">OUTPUTS</span></span>

### <span data-ttu-id="29dfb-139">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="29dfb-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="29dfb-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29dfb-140">NOTES</span></span>

<span data-ttu-id="29dfb-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="29dfb-141">ALIASES</span></span>

<span data-ttu-id="29dfb-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="29dfb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29dfb-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="29dfb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29dfb-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="29dfb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29dfb-145">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="29dfb-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29dfb-146">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="29dfb-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="29dfb-147">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="29dfb-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="29dfb-148">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="29dfb-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="29dfb-149">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="29dfb-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="29dfb-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="29dfb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29dfb-151">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="29dfb-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="29dfb-152">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="29dfb-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="29dfb-153">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="29dfb-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="29dfb-154">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29dfb-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="29dfb-155">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="29dfb-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="29dfb-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29dfb-156">RELATED LINKS</span></span>
