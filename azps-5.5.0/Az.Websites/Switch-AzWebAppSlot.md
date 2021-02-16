---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207438"
---
# <span data-ttu-id="bb04e-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb04e-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="bb04e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb04e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb04e-103">Két bővítőhely felcserélve webalkalmazással</span><span class="sxs-lookup"><span data-stu-id="bb04e-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="bb04e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bb04e-104">SYNTAX</span></span>

### <span data-ttu-id="bb04e-105">S1</span><span class="sxs-lookup"><span data-stu-id="bb04e-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb04e-106">S2</span><span class="sxs-lookup"><span data-stu-id="bb04e-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb04e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bb04e-107">DESCRIPTION</span></span>
<span data-ttu-id="bb04e-108">A **Switch-AzWebAppS slot** két, Az Azure Web Apphoz társított résidőt vált át.</span><span class="sxs-lookup"><span data-stu-id="bb04e-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="bb04e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bb04e-109">EXAMPLES</span></span>

### <span data-ttu-id="bb04e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="bb04e-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="bb04e-111">Ez a parancs a Default-Web-WestUS erőforráscsoporthoz társított Web App ContosoWebApp "destinations slot" (célhely) helyére vált</span><span class="sxs-lookup"><span data-stu-id="bb04e-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="bb04e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb04e-112">PARAMETERS</span></span>

### <span data-ttu-id="bb04e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb04e-113">-DefaultProfile</span></span>
<span data-ttu-id="bb04e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb04e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb04e-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="bb04e-115">-DestinationSlotName</span></span>
<span data-ttu-id="bb04e-116">Célhely neve</span><span class="sxs-lookup"><span data-stu-id="bb04e-116">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb04e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bb04e-117">-Name</span></span>
<span data-ttu-id="bb04e-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="bb04e-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb04e-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="bb04e-119">-PreserveVnet</span></span>
<span data-ttu-id="bb04e-120">Vnet-logikai logikai konzerv megőrzése</span><span class="sxs-lookup"><span data-stu-id="bb04e-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb04e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb04e-121">-ResourceGroupName</span></span>
<span data-ttu-id="bb04e-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="bb04e-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb04e-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="bb04e-123">-SourceSlotName</span></span>
<span data-ttu-id="bb04e-124">Forráshely neve</span><span class="sxs-lookup"><span data-stu-id="bb04e-124">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb04e-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="bb04e-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="bb04e-126">Swap With Preview Action</span><span class="sxs-lookup"><span data-stu-id="bb04e-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb04e-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bb04e-127">-WebApp</span></span>
<span data-ttu-id="bb04e-128">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="bb04e-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb04e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb04e-129">-Confirm</span></span>
<span data-ttu-id="bb04e-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bb04e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb04e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb04e-131">-WhatIf</span></span>
<span data-ttu-id="bb04e-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bb04e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb04e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb04e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb04e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb04e-134">CommonParameters</span></span>
<span data-ttu-id="bb04e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb04e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb04e-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb04e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb04e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb04e-137">INPUTS</span></span>

### <span data-ttu-id="bb04e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bb04e-138">System.String</span></span>

### <span data-ttu-id="bb04e-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="bb04e-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bb04e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb04e-140">OUTPUTS</span></span>

### <span data-ttu-id="bb04e-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="bb04e-141">System.Void</span></span>

## <span data-ttu-id="bb04e-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bb04e-142">NOTES</span></span>

## <span data-ttu-id="bb04e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb04e-143">RELATED LINKS</span></span>
