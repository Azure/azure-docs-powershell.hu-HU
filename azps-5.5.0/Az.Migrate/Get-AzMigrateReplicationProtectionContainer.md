---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: fbee443cf8f24737ea6da78be347beac48d7e588
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157395"
---
# <span data-ttu-id="cb805-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cb805-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="cb805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb805-102">SYNOPSIS</span></span>
<span data-ttu-id="cb805-103">Egy védelmi tároló adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cb805-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="cb805-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb805-104">SYNTAX</span></span>

### <span data-ttu-id="cb805-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb805-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb805-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="cb805-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb805-107">Lista</span><span class="sxs-lookup"><span data-stu-id="cb805-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cb805-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb805-108">DESCRIPTION</span></span>
<span data-ttu-id="cb805-109">Egy védelmi tároló adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cb805-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="cb805-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb805-110">EXAMPLES</span></span>

### <span data-ttu-id="cb805-111">1. példa: A tárolóban és a szövetben található összes védelmi tároló felsorolása</span><span class="sxs-lookup"><span data-stu-id="cb805-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="cb805-112">Az összes listája.</span><span class="sxs-lookup"><span data-stu-id="cb805-112">Lists all.</span></span>

### <span data-ttu-id="cb805-113">2. példa: Adott tároló lekérte</span><span class="sxs-lookup"><span data-stu-id="cb805-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="cb805-114">Konkrétat kap.</span><span class="sxs-lookup"><span data-stu-id="cb805-114">Gets a specific one.</span></span>

## <span data-ttu-id="cb805-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb805-115">PARAMETERS</span></span>

### <span data-ttu-id="cb805-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb805-116">-DefaultProfile</span></span>
<span data-ttu-id="cb805-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb805-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb805-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="cb805-118">-FabricName</span></span>
<span data-ttu-id="cb805-119">Anyagnév.</span><span class="sxs-lookup"><span data-stu-id="cb805-119">Fabric name.</span></span>

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

### <span data-ttu-id="cb805-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="cb805-120">-ProtectionContainerName</span></span>
<span data-ttu-id="cb805-121">Védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="cb805-121">Protection container name.</span></span>

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

### <span data-ttu-id="cb805-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb805-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb805-123">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="cb805-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="cb805-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cb805-124">-ResourceName</span></span>
<span data-ttu-id="cb805-125">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="cb805-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="cb805-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb805-126">-SubscriptionId</span></span>
<span data-ttu-id="cb805-127">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="cb805-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="cb805-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb805-128">CommonParameters</span></span>
<span data-ttu-id="cb805-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb805-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb805-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb805-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb805-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb805-131">INPUTS</span></span>

## <span data-ttu-id="cb805-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb805-132">OUTPUTS</span></span>

### <span data-ttu-id="cb805-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cb805-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="cb805-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb805-134">NOTES</span></span>

<span data-ttu-id="cb805-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cb805-135">ALIASES</span></span>

## <span data-ttu-id="cb805-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb805-136">RELATED LINKS</span></span>

