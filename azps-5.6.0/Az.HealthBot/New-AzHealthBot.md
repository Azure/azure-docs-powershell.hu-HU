---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: b9c4e4cd55f81449497b0d397574c3eeec64d2d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013222"
---
# <span data-ttu-id="b07a1-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="b07a1-101">New-AzHealthBot</span></span>

## <span data-ttu-id="b07a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b07a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b07a1-103">Hozzon létre egy új HealthBotot.</span><span class="sxs-lookup"><span data-stu-id="b07a1-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="b07a1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b07a1-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b07a1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b07a1-105">DESCRIPTION</span></span>
<span data-ttu-id="b07a1-106">Hozzon létre egy új HealthBotot.</span><span class="sxs-lookup"><span data-stu-id="b07a1-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="b07a1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b07a1-107">EXAMPLES</span></span>

### <span data-ttu-id="b07a1-108">1. példa: Új HealthBot létrehozása</span><span class="sxs-lookup"><span data-stu-id="b07a1-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="b07a1-109">Új HealthBot alapértelmezés szerint</span><span class="sxs-lookup"><span data-stu-id="b07a1-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="b07a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b07a1-110">PARAMETERS</span></span>

### <span data-ttu-id="b07a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b07a1-111">-AsJob</span></span>
<span data-ttu-id="b07a1-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="b07a1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b07a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07a1-113">-DefaultProfile</span></span>
<span data-ttu-id="b07a1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b07a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b07a1-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b07a1-115">-Location</span></span>
<span data-ttu-id="b07a1-116">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="b07a1-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="b07a1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b07a1-117">-Name</span></span>
<span data-ttu-id="b07a1-118">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b07a1-118">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07a1-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b07a1-119">-NoWait</span></span>
<span data-ttu-id="b07a1-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="b07a1-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b07a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="b07a1-122">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b07a1-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="b07a1-123">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="b07a1-123">-Sku</span></span>
<span data-ttu-id="b07a1-124">A HealthBot termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="b07a1-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07a1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b07a1-125">-SubscriptionId</span></span>
<span data-ttu-id="b07a1-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b07a1-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b07a1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b07a1-127">-Tag</span></span>
<span data-ttu-id="b07a1-128">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="b07a1-128">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07a1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b07a1-129">-Confirm</span></span>
<span data-ttu-id="b07a1-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b07a1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07a1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b07a1-131">-WhatIf</span></span>
<span data-ttu-id="b07a1-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b07a1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b07a1-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b07a1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07a1-134">CommonParameters</span></span>
<span data-ttu-id="b07a1-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07a1-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b07a1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07a1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b07a1-137">INPUTS</span></span>

## <span data-ttu-id="b07a1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b07a1-138">OUTPUTS</span></span>

### <span data-ttu-id="b07a1-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="b07a1-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="b07a1-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b07a1-140">NOTES</span></span>

<span data-ttu-id="b07a1-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b07a1-141">ALIASES</span></span>

## <span data-ttu-id="b07a1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b07a1-142">RELATED LINKS</span></span>

