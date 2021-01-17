---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371026"
---
# <span data-ttu-id="4a86b-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="4a86b-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="4a86b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a86b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a86b-103">Létrehoz egy új áttelepítési projektet.</span><span class="sxs-lookup"><span data-stu-id="4a86b-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="4a86b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4a86b-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a86b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4a86b-105">DESCRIPTION</span></span>
<span data-ttu-id="4a86b-106">Létrehoz egy új áttelepítési projektet.</span><span class="sxs-lookup"><span data-stu-id="4a86b-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="4a86b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4a86b-107">EXAMPLES</span></span>

### <span data-ttu-id="4a86b-108">1. példa: Létrehozás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a86b-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="4a86b-109">Új projekt áttelepítésének módszere.</span><span class="sxs-lookup"><span data-stu-id="4a86b-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="4a86b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a86b-110">PARAMETERS</span></span>

### <span data-ttu-id="4a86b-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="4a86b-111">-ETag</span></span>
<span data-ttu-id="4a86b-112">A VMware számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a86b-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="4a86b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="4a86b-113">-Location</span></span>
<span data-ttu-id="4a86b-114">A VMware számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a86b-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="4a86b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4a86b-115">-Name</span></span>
<span data-ttu-id="4a86b-116">A projekt nevét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4a86b-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="4a86b-117">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="4a86b-117">-Property</span></span>
<span data-ttu-id="4a86b-118">A projekt tulajdonságainak megadása.</span><span class="sxs-lookup"><span data-stu-id="4a86b-118">Specifies the project properties.</span></span>
<span data-ttu-id="4a86b-119">A szerkezetről a NOTES (JEGYZETEK) szakaszban találhatók a PROPERTY properties (TULAJDONSÁGtulajdonságok) című szakaszban, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="4a86b-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a86b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a86b-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a86b-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a86b-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="4a86b-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a86b-122">-SubscriptionId</span></span>
<span data-ttu-id="4a86b-123">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a86b-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="4a86b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a86b-124">-Confirm</span></span>
<span data-ttu-id="4a86b-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4a86b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a86b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a86b-126">-WhatIf</span></span>
<span data-ttu-id="4a86b-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4a86b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a86b-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a86b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a86b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a86b-129">CommonParameters</span></span>
<span data-ttu-id="4a86b-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a86b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a86b-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a86b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a86b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a86b-132">INPUTS</span></span>

## <span data-ttu-id="4a86b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a86b-133">OUTPUTS</span></span>

## <span data-ttu-id="4a86b-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4a86b-134">NOTES</span></span>

<span data-ttu-id="4a86b-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4a86b-135">ALIASES</span></span>

<span data-ttu-id="4a86b-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4a86b-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a86b-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="4a86b-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a86b-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a86b-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a86b-139">TULAJDONSÁG: <IMigrateProjectProperties> A projekttulajdonságok megadása.</span><span class="sxs-lookup"><span data-stu-id="4a86b-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="4a86b-140">`[ProvisioningState <ProvisioningState?>]`: A projekt átépítési állapota.</span><span class="sxs-lookup"><span data-stu-id="4a86b-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="4a86b-141">`[RegisteredTool <String[]>]`: Beállítja vagy beállítja a projekt áttelepítéséhez regisztrált eszközök listáját.</span><span class="sxs-lookup"><span data-stu-id="4a86b-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="4a86b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a86b-142">RELATED LINKS</span></span>

