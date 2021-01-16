---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466329"
---
# <span data-ttu-id="19d17-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="19d17-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="19d17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19d17-102">SYNOPSIS</span></span>
<span data-ttu-id="19d17-103">Egy védelmi tároló megfeleltetésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19d17-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="19d17-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19d17-104">SYNTAX</span></span>

### <span data-ttu-id="19d17-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19d17-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19d17-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="19d17-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19d17-107">Lista</span><span class="sxs-lookup"><span data-stu-id="19d17-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="19d17-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19d17-108">DESCRIPTION</span></span>
<span data-ttu-id="19d17-109">Egy védelmi tároló megfeleltetésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19d17-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="19d17-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19d17-110">EXAMPLES</span></span>

### <span data-ttu-id="19d17-111">1. példa: Adott megfeleltetés lekérte</span><span class="sxs-lookup"><span data-stu-id="19d17-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="19d17-112">Lekérte a megfeleltetés részleteit.</span><span class="sxs-lookup"><span data-stu-id="19d17-112">Get a mapping detail.</span></span>

## <span data-ttu-id="19d17-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19d17-113">PARAMETERS</span></span>

### <span data-ttu-id="19d17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d17-114">-DefaultProfile</span></span>
<span data-ttu-id="19d17-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19d17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19d17-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="19d17-116">-FabricName</span></span>
<span data-ttu-id="19d17-117">Anyagnév.</span><span class="sxs-lookup"><span data-stu-id="19d17-117">Fabric name.</span></span>

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

### <span data-ttu-id="19d17-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="19d17-118">-MappingName</span></span>
<span data-ttu-id="19d17-119">Protection Container mapping name.</span><span class="sxs-lookup"><span data-stu-id="19d17-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="19d17-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="19d17-120">-ProtectionContainerName</span></span>
<span data-ttu-id="19d17-121">Védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="19d17-121">Protection container name.</span></span>

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

### <span data-ttu-id="19d17-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d17-122">-ResourceGroupName</span></span>
<span data-ttu-id="19d17-123">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="19d17-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="19d17-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="19d17-124">-ResourceName</span></span>
<span data-ttu-id="19d17-125">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="19d17-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="19d17-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19d17-126">-SubscriptionId</span></span>
<span data-ttu-id="19d17-127">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="19d17-127">The subscription Id.</span></span>

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

### <span data-ttu-id="19d17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d17-128">CommonParameters</span></span>
<span data-ttu-id="19d17-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d17-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19d17-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d17-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19d17-131">INPUTS</span></span>

## <span data-ttu-id="19d17-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19d17-132">OUTPUTS</span></span>

### <span data-ttu-id="19d17-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="19d17-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="19d17-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19d17-134">NOTES</span></span>

<span data-ttu-id="19d17-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="19d17-135">ALIASES</span></span>

## <span data-ttu-id="19d17-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19d17-136">RELATED LINKS</span></span>

