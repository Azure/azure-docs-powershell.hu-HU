---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182436"
---
# <span data-ttu-id="3007e-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3007e-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="3007e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3007e-102">SYNOPSIS</span></span>
<span data-ttu-id="3007e-103">Két bővítőhely cseréje webalkalmazással</span><span class="sxs-lookup"><span data-stu-id="3007e-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="3007e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3007e-104">SYNTAX</span></span>

### <span data-ttu-id="3007e-105">S1</span><span class="sxs-lookup"><span data-stu-id="3007e-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3007e-106">S2</span><span class="sxs-lookup"><span data-stu-id="3007e-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3007e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3007e-107">DESCRIPTION</span></span>
<span data-ttu-id="3007e-108">A **kapcsoló – AzWebAppSlot** két bővítőhelyet vált át az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="3007e-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="3007e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3007e-109">EXAMPLES</span></span>

### <span data-ttu-id="3007e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3007e-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="3007e-111">Ez a parancs a "sourceslot" bővítőhely "destinationslot" típusú, az erőforráscsoport alapértelmezett ContosoWebApp társított Web App-WestUS</span><span class="sxs-lookup"><span data-stu-id="3007e-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3007e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3007e-112">PARAMETERS</span></span>

### <span data-ttu-id="3007e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3007e-113">-DefaultProfile</span></span>
<span data-ttu-id="3007e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3007e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3007e-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="3007e-115">-DestinationSlotName</span></span>
<span data-ttu-id="3007e-116">Cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="3007e-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="3007e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3007e-117">-Name</span></span>
<span data-ttu-id="3007e-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="3007e-118">WebApp Name</span></span>

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

### <span data-ttu-id="3007e-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="3007e-119">-PreserveVnet</span></span>
<span data-ttu-id="3007e-120">A vnet logikai értékének megőrzése</span><span class="sxs-lookup"><span data-stu-id="3007e-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="3007e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3007e-121">-ResourceGroupName</span></span>
<span data-ttu-id="3007e-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3007e-122">Resource Group Name</span></span>

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

### <span data-ttu-id="3007e-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="3007e-123">-SourceSlotName</span></span>
<span data-ttu-id="3007e-124">Forrás bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="3007e-124">Source Slot Name</span></span>

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

### <span data-ttu-id="3007e-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="3007e-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="3007e-126">Csere előzetes eljárással</span><span class="sxs-lookup"><span data-stu-id="3007e-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="3007e-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3007e-127">-WebApp</span></span>
<span data-ttu-id="3007e-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="3007e-128">WebApp Object</span></span>

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

### <span data-ttu-id="3007e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3007e-129">-Confirm</span></span>
<span data-ttu-id="3007e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3007e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3007e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3007e-131">-WhatIf</span></span>
<span data-ttu-id="3007e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3007e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3007e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3007e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3007e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3007e-134">CommonParameters</span></span>
<span data-ttu-id="3007e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3007e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3007e-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3007e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3007e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3007e-137">INPUTS</span></span>

### <span data-ttu-id="3007e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3007e-138">System.String</span></span>

### <span data-ttu-id="3007e-139">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3007e-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3007e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3007e-140">OUTPUTS</span></span>

### <span data-ttu-id="3007e-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="3007e-141">System.Void</span></span>

## <span data-ttu-id="3007e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3007e-142">NOTES</span></span>

## <span data-ttu-id="3007e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3007e-143">RELATED LINKS</span></span>
