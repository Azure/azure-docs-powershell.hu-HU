---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203583"
---
# <span data-ttu-id="69b0f-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="69b0f-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="69b0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="69b0f-103">Létrehoz egy új áttelepítési projektet.</span><span class="sxs-lookup"><span data-stu-id="69b0f-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="69b0f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69b0f-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69b0f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="69b0f-106">Létrehoz egy új áttelepítési projektet.</span><span class="sxs-lookup"><span data-stu-id="69b0f-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="69b0f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="69b0f-108">1. példa: Létrehozás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69b0f-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="69b0f-109">Új projekt áttelepítésének módszere.</span><span class="sxs-lookup"><span data-stu-id="69b0f-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="69b0f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69b0f-110">PARAMETERS</span></span>

### <span data-ttu-id="69b0f-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="69b0f-111">-ETag</span></span>
<span data-ttu-id="69b0f-112">A VMware számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b0f-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="69b0f-113">-Location</span><span class="sxs-lookup"><span data-stu-id="69b0f-113">-Location</span></span>
<span data-ttu-id="69b0f-114">A VMware számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b0f-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="69b0f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="69b0f-115">-Name</span></span>
<span data-ttu-id="69b0f-116">A projekt nevét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="69b0f-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="69b0f-117">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="69b0f-117">-Property</span></span>
<span data-ttu-id="69b0f-118">A projekt tulajdonságainak megadása.</span><span class="sxs-lookup"><span data-stu-id="69b0f-118">Specifies the project properties.</span></span>
<span data-ttu-id="69b0f-119">A szerkezetről a NOTES (JEGYZETEK) szakaszban találhatók a TULAJDONSÁGtulajdonságok, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="69b0f-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="69b0f-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b0f-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="69b0f-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69b0f-122">-SubscriptionId</span></span>
<span data-ttu-id="69b0f-123">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b0f-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="69b0f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69b0f-124">-Confirm</span></span>
<span data-ttu-id="69b0f-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69b0f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b0f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b0f-126">-WhatIf</span></span>
<span data-ttu-id="69b0f-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69b0f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b0f-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69b0f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b0f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b0f-129">CommonParameters</span></span>
<span data-ttu-id="69b0f-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b0f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b0f-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69b0f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b0f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69b0f-132">INPUTS</span></span>

## <span data-ttu-id="69b0f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69b0f-133">OUTPUTS</span></span>

## <span data-ttu-id="69b0f-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69b0f-134">NOTES</span></span>

<span data-ttu-id="69b0f-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="69b0f-135">ALIASES</span></span>

<span data-ttu-id="69b0f-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="69b0f-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69b0f-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="69b0f-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69b0f-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69b0f-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69b0f-139">TULAJDONSÁG: <IMigrateProjectProperties> A projekttulajdonságok megadása.</span><span class="sxs-lookup"><span data-stu-id="69b0f-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="69b0f-140">`[ProvisioningState <ProvisioningState?>]`: A projekt áttelepítésének kiépítési állapota.</span><span class="sxs-lookup"><span data-stu-id="69b0f-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="69b0f-141">`[RegisteredTool <String[]>]`: Beállítja vagy beállítja a projekt áttelepítéséhez regisztrált eszközök listáját.</span><span class="sxs-lookup"><span data-stu-id="69b0f-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="69b0f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69b0f-142">RELATED LINKS</span></span>

