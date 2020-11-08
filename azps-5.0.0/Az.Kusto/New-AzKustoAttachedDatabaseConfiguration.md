---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194708"
---
# <span data-ttu-id="4acd9-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="4acd9-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="4acd9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4acd9-102">SYNOPSIS</span></span>
<span data-ttu-id="4acd9-103">Csatolt adatbázis-konfiguráció létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="4acd9-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="4acd9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4acd9-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4acd9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4acd9-105">DESCRIPTION</span></span>
<span data-ttu-id="4acd9-106">Csatolt adatbázis-konfiguráció létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="4acd9-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="4acd9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4acd9-107">EXAMPLES</span></span>

### <span data-ttu-id="4acd9-108">Példa 1: új AttachedDatabaseConfiguration létrehozása</span><span class="sxs-lookup"><span data-stu-id="4acd9-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="4acd9-109">A fenti parancs létrehoz egy írásvédett adatbázist "mykustodatabase" a cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="4acd9-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="4acd9-110">Az "mykustodatabase" adatbázis a "testnewkustocluster" cluster "" adatbázisból következik</span><span class="sxs-lookup"><span data-stu-id="4acd9-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="4acd9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4acd9-111">PARAMETERS</span></span>

### <span data-ttu-id="4acd9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4acd9-112">-AsJob</span></span>
<span data-ttu-id="4acd9-113">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="4acd9-113">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-114">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="4acd9-114">-ClusterName</span></span>
<span data-ttu-id="4acd9-115">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="4acd9-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4acd9-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="4acd9-116">-ClusterResourceId</span></span>
<span data-ttu-id="4acd9-117">Annak a fürtnek az erőforrás-azonosítója, amelyben a csatolni kívánt adatbázisok találhatók.</span><span class="sxs-lookup"><span data-stu-id="4acd9-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4acd9-118">-DatabaseName</span></span>
<span data-ttu-id="4acd9-119">Annak az adatbázisnak a neve, amelyet csatolni szeretne, használja \* ha a jelenlegi és a jövőbeli adatbázisokat szeretné követni.</span><span class="sxs-lookup"><span data-stu-id="4acd9-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="4acd9-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="4acd9-121">A megbízók alapértelmezett módosítási típusa</span><span class="sxs-lookup"><span data-stu-id="4acd9-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4acd9-122">-DefaultProfile</span></span>
<span data-ttu-id="4acd9-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4acd9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4acd9-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="4acd9-124">-Location</span></span>
<span data-ttu-id="4acd9-125">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4acd9-125">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4acd9-126">-Name</span></span>
<span data-ttu-id="4acd9-127">A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="4acd9-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-128">-Várva</span><span class="sxs-lookup"><span data-stu-id="4acd9-128">-NoWait</span></span>
<span data-ttu-id="4acd9-129">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="4acd9-129">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4acd9-130">-ResourceGroupName</span></span>
<span data-ttu-id="4acd9-131">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4acd9-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4acd9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4acd9-132">-SubscriptionId</span></span>
<span data-ttu-id="4acd9-133">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4acd9-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4acd9-134">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4acd9-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4acd9-135">-Confirm</span></span>
<span data-ttu-id="4acd9-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4acd9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4acd9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4acd9-137">-WhatIf</span></span>
<span data-ttu-id="4acd9-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4acd9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4acd9-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4acd9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4acd9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4acd9-140">CommonParameters</span></span>
<span data-ttu-id="4acd9-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4acd9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4acd9-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4acd9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4acd9-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4acd9-143">INPUTS</span></span>

## <span data-ttu-id="4acd9-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4acd9-144">OUTPUTS</span></span>

### <span data-ttu-id="4acd9-145">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="4acd9-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="4acd9-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4acd9-146">NOTES</span></span>

<span data-ttu-id="4acd9-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4acd9-147">ALIASES</span></span>

## <span data-ttu-id="4acd9-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4acd9-148">RELATED LINKS</span></span>
