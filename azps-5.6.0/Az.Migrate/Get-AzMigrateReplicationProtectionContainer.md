---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: 7a1cec73706d1ed799966bc3d97da06867139c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934042"
---
# <span data-ttu-id="b3a41-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b3a41-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="b3a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a41-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a41-103">Egy védelmi tároló adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b3a41-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="b3a41-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3a41-104">SYNTAX</span></span>

### <span data-ttu-id="b3a41-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3a41-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3a41-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="b3a41-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3a41-107">Lista</span><span class="sxs-lookup"><span data-stu-id="b3a41-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b3a41-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3a41-108">DESCRIPTION</span></span>
<span data-ttu-id="b3a41-109">Egy védelmi tároló adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b3a41-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="b3a41-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3a41-110">EXAMPLES</span></span>

### <span data-ttu-id="b3a41-111">1. példa: A tárolóban és a szövetben található összes védelmi tároló felsorolása</span><span class="sxs-lookup"><span data-stu-id="b3a41-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="b3a41-112">Az összes listája.</span><span class="sxs-lookup"><span data-stu-id="b3a41-112">Lists all.</span></span>

### <span data-ttu-id="b3a41-113">2. példa: Adott tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="b3a41-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="b3a41-114">Konkrétat kap.</span><span class="sxs-lookup"><span data-stu-id="b3a41-114">Gets a specific one.</span></span>

## <span data-ttu-id="b3a41-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3a41-115">PARAMETERS</span></span>

### <span data-ttu-id="b3a41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a41-116">-DefaultProfile</span></span>
<span data-ttu-id="b3a41-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3a41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a41-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="b3a41-118">-FabricName</span></span>
<span data-ttu-id="b3a41-119">Anyagnév.</span><span class="sxs-lookup"><span data-stu-id="b3a41-119">Fabric name.</span></span>

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

### <span data-ttu-id="b3a41-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="b3a41-120">-ProtectionContainerName</span></span>
<span data-ttu-id="b3a41-121">Védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="b3a41-121">Protection container name.</span></span>

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

### <span data-ttu-id="b3a41-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a41-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3a41-123">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="b3a41-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="b3a41-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b3a41-124">-ResourceName</span></span>
<span data-ttu-id="b3a41-125">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="b3a41-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="b3a41-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3a41-126">-SubscriptionId</span></span>
<span data-ttu-id="b3a41-127">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="b3a41-127">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a41-128">CommonParameters</span></span>
<span data-ttu-id="b3a41-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a41-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a41-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a41-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3a41-131">INPUTS</span></span>

## <span data-ttu-id="b3a41-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3a41-132">OUTPUTS</span></span>

### <span data-ttu-id="b3a41-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b3a41-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="b3a41-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3a41-134">NOTES</span></span>

<span data-ttu-id="b3a41-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b3a41-135">ALIASES</span></span>

## <span data-ttu-id="b3a41-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3a41-136">RELATED LINKS</span></span>

