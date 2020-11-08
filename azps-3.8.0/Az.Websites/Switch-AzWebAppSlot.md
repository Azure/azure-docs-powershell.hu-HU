---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012586"
---
# <span data-ttu-id="f1a6c-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f1a6c-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="f1a6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a6c-103">Két bővítőhely cseréje webalkalmazással</span><span class="sxs-lookup"><span data-stu-id="f1a6c-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="f1a6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1a6c-104">SYNTAX</span></span>

### <span data-ttu-id="f1a6c-105">S1</span><span class="sxs-lookup"><span data-stu-id="f1a6c-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a6c-106">S2</span><span class="sxs-lookup"><span data-stu-id="f1a6c-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a6c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1a6c-107">DESCRIPTION</span></span>
<span data-ttu-id="f1a6c-108">A **kapcsoló – AzWebAppSlot** két bővítőhelyet vált át az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="f1a6c-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="f1a6c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f1a6c-109">EXAMPLES</span></span>

### <span data-ttu-id="f1a6c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f1a6c-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="f1a6c-111">Ez a parancs a "sourceslot" bővítőhely "destinationslot" típusú, az erőforráscsoport alapértelmezett ContosoWebApp társított Web App-WestUS</span><span class="sxs-lookup"><span data-stu-id="f1a6c-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="f1a6c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1a6c-112">PARAMETERS</span></span>

### <span data-ttu-id="f1a6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a6c-113">-DefaultProfile</span></span>
<span data-ttu-id="f1a6c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1a6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1a6c-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="f1a6c-115">-DestinationSlotName</span></span>
<span data-ttu-id="f1a6c-116">Cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="f1a6c-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="f1a6c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1a6c-117">-Name</span></span>
<span data-ttu-id="f1a6c-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f1a6c-118">WebApp Name</span></span>

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

### <span data-ttu-id="f1a6c-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="f1a6c-119">-PreserveVnet</span></span>
<span data-ttu-id="f1a6c-120">A vnet logikai értékének megőrzése</span><span class="sxs-lookup"><span data-stu-id="f1a6c-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="f1a6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1a6c-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f1a6c-122">Resource Group Name</span></span>

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

### <span data-ttu-id="f1a6c-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="f1a6c-123">-SourceSlotName</span></span>
<span data-ttu-id="f1a6c-124">Forrás bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="f1a6c-124">Source Slot Name</span></span>

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

### <span data-ttu-id="f1a6c-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="f1a6c-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="f1a6c-126">Csere előzetes eljárással</span><span class="sxs-lookup"><span data-stu-id="f1a6c-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="f1a6c-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f1a6c-127">-WebApp</span></span>
<span data-ttu-id="f1a6c-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="f1a6c-128">WebApp Object</span></span>

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

### <span data-ttu-id="f1a6c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1a6c-129">-Confirm</span></span>
<span data-ttu-id="f1a6c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1a6c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a6c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a6c-131">-WhatIf</span></span>
<span data-ttu-id="f1a6c-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1a6c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a6c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1a6c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a6c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a6c-134">CommonParameters</span></span>
<span data-ttu-id="f1a6c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1a6c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a6c-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a6c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a6c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1a6c-137">INPUTS</span></span>

### <span data-ttu-id="f1a6c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a6c-138">System.String</span></span>

### <span data-ttu-id="f1a6c-139">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f1a6c-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f1a6c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1a6c-140">OUTPUTS</span></span>

### <span data-ttu-id="f1a6c-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="f1a6c-141">System.Void</span></span>

## <span data-ttu-id="f1a6c-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1a6c-142">NOTES</span></span>

## <span data-ttu-id="f1a6c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1a6c-143">RELATED LINKS</span></span>
