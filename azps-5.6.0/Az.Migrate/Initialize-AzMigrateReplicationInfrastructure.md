---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/initialize-azmigratereplicationinfrastructure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
ms.openlocfilehash: 27206ac1c4e256efcd4093c8cdc9647b6059b3ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934009"
---
# <span data-ttu-id="c25f1-101">Initialize-AzMigrateReplicationInfrastructure</span><span class="sxs-lookup"><span data-stu-id="c25f1-101">Initialize-AzMigrateReplicationInfrastructure</span></span>

## <span data-ttu-id="c25f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c25f1-103">Inicializálja a projekt áttelepítéséhez szükséges infrastruktúrát.</span><span class="sxs-lookup"><span data-stu-id="c25f1-103">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="c25f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c25f1-104">SYNTAX</span></span>

```
Initialize-AzMigrateReplicationInfrastructure -ProjectName <String> -ResourceGroupName <String>
 -Scenario <String> -TargetRegion <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c25f1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c25f1-105">DESCRIPTION</span></span>
<span data-ttu-id="c25f1-106">A Initialize-AzMigrateReplicationInfrastructure parancsmag inicializálja a projekt áttelepítéséhez szükséges infrastruktúrát.</span><span class="sxs-lookup"><span data-stu-id="c25f1-106">The Initialize-AzMigrateReplicationInfrastructure cmdlet initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="c25f1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c25f1-107">EXAMPLES</span></span>

### <span data-ttu-id="c25f1-108">1. példa: A projekt áttelepítéséhez szükséges infrastruktúra inicializálása.</span><span class="sxs-lookup"><span data-stu-id="c25f1-108">Example 1: Initialises the infrastructure for the migrate project.</span></span>
```powershell
PS C:\> Initialize-AzMigrateReplicationInfrastructure.ps1 -ResourceGroupName TestRG  -ProjectName TestProject -Vmwareagentless -TargetRegion centralus

True
```

<span data-ttu-id="c25f1-109">Inicializálja a projekt áttelepítéséhez szükséges infrastruktúrát.</span><span class="sxs-lookup"><span data-stu-id="c25f1-109">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="c25f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c25f1-110">PARAMETERS</span></span>

### <span data-ttu-id="c25f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25f1-111">-DefaultProfile</span></span>
<span data-ttu-id="c25f1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c25f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25f1-113">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c25f1-113">-ProjectName</span></span>
<span data-ttu-id="c25f1-114">A kiszolgáló áttelepítéséhez használt Azure-áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="c25f1-114">Specifies the name of the Azure Migrate project to be used for server migration.</span></span>

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

### <span data-ttu-id="c25f1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25f1-115">-ResourceGroupName</span></span>
<span data-ttu-id="c25f1-116">Az aktuális előfizetés azure-áttelepítési projekt erőforráscsoportját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c25f1-116">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="c25f1-117">-Scenario</span><span class="sxs-lookup"><span data-stu-id="c25f1-117">-Scenario</span></span>
<span data-ttu-id="c25f1-118">Azt a kiszolgáló-áttelepítési forgatókönyvet adja meg, amelyben a replikációs infrastruktúrát inicializálni kell.</span><span class="sxs-lookup"><span data-stu-id="c25f1-118">Specifies the server migration scenario for which the replication infrastructure needs to be initialized.</span></span>

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

### <span data-ttu-id="c25f1-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c25f1-119">-SubscriptionId</span></span>
<span data-ttu-id="c25f1-120">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c25f1-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c25f1-121">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="c25f1-121">-TargetRegion</span></span>
<span data-ttu-id="c25f1-122">A kiszolgáló áttelepítéséhez a cél Azure-régiót adja meg.</span><span class="sxs-lookup"><span data-stu-id="c25f1-122">Specifies the target Azure region for server migrations.</span></span>

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

### <span data-ttu-id="c25f1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c25f1-123">-Confirm</span></span>
<span data-ttu-id="c25f1-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c25f1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25f1-125">-WhatIf</span></span>
<span data-ttu-id="c25f1-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c25f1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c25f1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c25f1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25f1-128">CommonParameters</span></span>
<span data-ttu-id="c25f1-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25f1-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c25f1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25f1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c25f1-131">INPUTS</span></span>

## <span data-ttu-id="c25f1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c25f1-132">OUTPUTS</span></span>

### <span data-ttu-id="c25f1-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c25f1-133">System.Boolean</span></span>

## <span data-ttu-id="c25f1-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c25f1-134">NOTES</span></span>

<span data-ttu-id="c25f1-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c25f1-135">ALIASES</span></span>

## <span data-ttu-id="c25f1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c25f1-136">RELATED LINKS</span></span>

