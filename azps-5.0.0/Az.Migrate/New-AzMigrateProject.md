---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194574"
---
# <span data-ttu-id="af9a1-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="af9a1-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="af9a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="af9a1-103">Új áttelepítés-projektet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="af9a1-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="af9a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af9a1-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af9a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="af9a1-106">Új áttelepítés-projektet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="af9a1-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="af9a1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af9a1-107">EXAMPLES</span></span>

### <span data-ttu-id="af9a1-108">Példa 1: Create (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af9a1-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="af9a1-109">Új áttelepítési projekt létrehozásának módszere.</span><span class="sxs-lookup"><span data-stu-id="af9a1-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="af9a1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af9a1-110">PARAMETERS</span></span>

### <span data-ttu-id="af9a1-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="af9a1-111">-ETag</span></span>
<span data-ttu-id="af9a1-112">A VMware Machine nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af9a1-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="af9a1-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="af9a1-113">-Location</span></span>
<span data-ttu-id="af9a1-114">A VMware Machine nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af9a1-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="af9a1-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af9a1-115">-Name</span></span>
<span data-ttu-id="af9a1-116">A projekt áttelepítési nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af9a1-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="af9a1-117">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="af9a1-117">-Property</span></span>
<span data-ttu-id="af9a1-118">A projekt tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="af9a1-118">Specifies the project properties.</span></span>
<span data-ttu-id="af9a1-119">A kivitelezéshez tekintse meg a tulajdonságok tulajdonságairól szóló megjegyzések szakaszt, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="af9a1-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="af9a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="af9a1-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af9a1-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="af9a1-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af9a1-122">-SubscriptionId</span></span>
<span data-ttu-id="af9a1-123">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="af9a1-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="af9a1-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af9a1-124">-Confirm</span></span>
<span data-ttu-id="af9a1-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af9a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9a1-126">-WhatIf</span></span>
<span data-ttu-id="af9a1-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af9a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9a1-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af9a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9a1-129">CommonParameters</span></span>
<span data-ttu-id="af9a1-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af9a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9a1-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="af9a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9a1-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af9a1-132">INPUTS</span></span>

## <span data-ttu-id="af9a1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af9a1-133">OUTPUTS</span></span>

## <span data-ttu-id="af9a1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af9a1-134">NOTES</span></span>

<span data-ttu-id="af9a1-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="af9a1-135">ALIASES</span></span>

<span data-ttu-id="af9a1-136">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="af9a1-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af9a1-137">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="af9a1-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af9a1-138">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="af9a1-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af9a1-139">TULAJDONSÁG <IMigrateProjectProperties> : a projekt tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="af9a1-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="af9a1-140">`[ProvisioningState <ProvisioningState?>]`: Az áttelepítési projekt létesítési állapota</span><span class="sxs-lookup"><span data-stu-id="af9a1-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="af9a1-141">`[RegisteredTool <String[]>]`: Beadja vagy beállítja az áttelepítési projektben regisztrált eszközök listáját.</span><span class="sxs-lookup"><span data-stu-id="af9a1-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="af9a1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af9a1-142">RELATED LINKS</span></span>

