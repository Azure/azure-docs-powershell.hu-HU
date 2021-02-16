---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 09284a91c5ea2f7561a867250a92c4cd0d96e8e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209255"
---
# <span data-ttu-id="b870b-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="b870b-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="b870b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b870b-102">SYNOPSIS</span></span>
<span data-ttu-id="b870b-103">Csatolt adatbázis-konfigurációt hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="b870b-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="b870b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b870b-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b870b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b870b-105">DESCRIPTION</span></span>
<span data-ttu-id="b870b-106">Csatolt adatbázis-konfigurációt hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="b870b-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="b870b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b870b-107">EXAMPLES</span></span>

### <span data-ttu-id="b870b-108">1. példa: Új AttachedDatabaseConfiguration létrehozása</span><span class="sxs-lookup"><span data-stu-id="b870b-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="b870b-109">A fenti parancs létrehoz egy ReadOnly adatbázist "mykustodatabase" a "testnewkustoclusterf" fürtben.</span><span class="sxs-lookup"><span data-stu-id="b870b-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="b870b-110">A "testnewkustocluster" fürt "mykustodatabase" adatbázisát követi.</span><span class="sxs-lookup"><span data-stu-id="b870b-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="b870b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b870b-111">PARAMETERS</span></span>

### <span data-ttu-id="b870b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b870b-112">-AsJob</span></span>
<span data-ttu-id="b870b-113">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="b870b-113">Run the command as a job</span></span>

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

### <span data-ttu-id="b870b-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b870b-114">-ClusterName</span></span>
<span data-ttu-id="b870b-115">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b870b-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b870b-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="b870b-116">-ClusterResourceId</span></span>
<span data-ttu-id="b870b-117">Annak a fürtnek az erőforrás-azonosítója, amelybe a csatolni szeretné az adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="b870b-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="b870b-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b870b-118">-DatabaseName</span></span>
<span data-ttu-id="b870b-119">A csatolni kívánt adatbázis neve a \*, ha az összes jelenlegi és jövőbeli adatbázist követni szeretné.</span><span class="sxs-lookup"><span data-stu-id="b870b-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="b870b-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="b870b-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="b870b-121">Az alapértelmezett principals módosítási típus</span><span class="sxs-lookup"><span data-stu-id="b870b-121">The default principals modification kind</span></span>

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

### <span data-ttu-id="b870b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b870b-122">-DefaultProfile</span></span>
<span data-ttu-id="b870b-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b870b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b870b-124">-Location</span><span class="sxs-lookup"><span data-stu-id="b870b-124">-Location</span></span>
<span data-ttu-id="b870b-125">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b870b-125">Resource location.</span></span>

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

### <span data-ttu-id="b870b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b870b-126">-Name</span></span>
<span data-ttu-id="b870b-127">A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="b870b-127">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="b870b-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b870b-128">-NoWait</span></span>
<span data-ttu-id="b870b-129">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="b870b-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b870b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b870b-130">-ResourceGroupName</span></span>
<span data-ttu-id="b870b-131">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b870b-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b870b-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b870b-132">-SubscriptionId</span></span>
<span data-ttu-id="b870b-133">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b870b-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b870b-134">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b870b-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b870b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b870b-135">-Confirm</span></span>
<span data-ttu-id="b870b-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b870b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b870b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b870b-137">-WhatIf</span></span>
<span data-ttu-id="b870b-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b870b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b870b-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b870b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b870b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b870b-140">CommonParameters</span></span>
<span data-ttu-id="b870b-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b870b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b870b-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b870b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b870b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b870b-143">INPUTS</span></span>

## <span data-ttu-id="b870b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b870b-144">OUTPUTS</span></span>

### <span data-ttu-id="b870b-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.iAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="b870b-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="b870b-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b870b-146">NOTES</span></span>

<span data-ttu-id="b870b-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b870b-147">ALIASES</span></span>

## <span data-ttu-id="b870b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b870b-148">RELATED LINKS</span></span>

