---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: dc39a7324f89e0a45efd4b631fb24a2e000d5e72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147810"
---
# <span data-ttu-id="54c6d-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="54c6d-101">New-AzHealthBot</span></span>

## <span data-ttu-id="54c6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="54c6d-103">Hozzon létre egy új HealthBotot.</span><span class="sxs-lookup"><span data-stu-id="54c6d-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="54c6d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="54c6d-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54c6d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="54c6d-105">DESCRIPTION</span></span>
<span data-ttu-id="54c6d-106">Hozzon létre egy új HealthBotot.</span><span class="sxs-lookup"><span data-stu-id="54c6d-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="54c6d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="54c6d-107">EXAMPLES</span></span>

### <span data-ttu-id="54c6d-108">1. példa: Új HealthBot létrehozása</span><span class="sxs-lookup"><span data-stu-id="54c6d-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="54c6d-109">Új HealthBot alapértelmezés szerint</span><span class="sxs-lookup"><span data-stu-id="54c6d-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="54c6d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54c6d-110">PARAMETERS</span></span>

### <span data-ttu-id="54c6d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54c6d-111">-AsJob</span></span>
<span data-ttu-id="54c6d-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="54c6d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="54c6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c6d-113">-DefaultProfile</span></span>
<span data-ttu-id="54c6d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54c6d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c6d-115">-Location</span><span class="sxs-lookup"><span data-stu-id="54c6d-115">-Location</span></span>
<span data-ttu-id="54c6d-116">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="54c6d-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="54c6d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="54c6d-117">-Name</span></span>
<span data-ttu-id="54c6d-118">A roboterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="54c6d-118">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="54c6d-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="54c6d-119">-NoWait</span></span>
<span data-ttu-id="54c6d-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="54c6d-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="54c6d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c6d-121">-ResourceGroupName</span></span>
<span data-ttu-id="54c6d-122">A roboterőforrás-csoport neve a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="54c6d-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="54c6d-123">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="54c6d-123">-Sku</span></span>
<span data-ttu-id="54c6d-124">A HealthBot termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="54c6d-124">The name of the HealthBot SKU</span></span>

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

### <span data-ttu-id="54c6d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54c6d-125">-SubscriptionId</span></span>
<span data-ttu-id="54c6d-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54c6d-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="54c6d-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="54c6d-127">-Tag</span></span>
<span data-ttu-id="54c6d-128">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="54c6d-128">Resource tags.</span></span>

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

### <span data-ttu-id="54c6d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54c6d-129">-Confirm</span></span>
<span data-ttu-id="54c6d-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="54c6d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c6d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c6d-131">-WhatIf</span></span>
<span data-ttu-id="54c6d-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="54c6d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c6d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54c6d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c6d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c6d-134">CommonParameters</span></span>
<span data-ttu-id="54c6d-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c6d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c6d-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54c6d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c6d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54c6d-137">INPUTS</span></span>

## <span data-ttu-id="54c6d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54c6d-138">OUTPUTS</span></span>

### <span data-ttu-id="54c6d-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.iHealthBot</span><span class="sxs-lookup"><span data-stu-id="54c6d-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="54c6d-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="54c6d-140">NOTES</span></span>

<span data-ttu-id="54c6d-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="54c6d-141">ALIASES</span></span>

## <span data-ttu-id="54c6d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54c6d-142">RELATED LINKS</span></span>

