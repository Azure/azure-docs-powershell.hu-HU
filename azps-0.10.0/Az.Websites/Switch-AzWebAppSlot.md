---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/switch-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: e30179ce2e9198729771d406d1963ff0048e05b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842645"
---
# <span data-ttu-id="ce68d-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ce68d-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="ce68d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce68d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce68d-103">Két bővítőhely cseréje webalkalmazással</span><span class="sxs-lookup"><span data-stu-id="ce68d-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="ce68d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce68d-104">SYNTAX</span></span>

### <span data-ttu-id="ce68d-105">S1</span><span class="sxs-lookup"><span data-stu-id="ce68d-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce68d-106">S2</span><span class="sxs-lookup"><span data-stu-id="ce68d-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce68d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce68d-107">DESCRIPTION</span></span>
<span data-ttu-id="ce68d-108">A **kapcsoló – AzWebAppSlot** két bővítőhelyet vált át az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="ce68d-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="ce68d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ce68d-109">EXAMPLES</span></span>

### <span data-ttu-id="ce68d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ce68d-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ce68d-111">Ez a parancs a "destinationslot" bővítőhely "sourceslot" bővítőhelyre vált a Web App ContosoWebApp, amely az erőforráscsoport alapértelmezett verziójában van társítva – web-WestUS</span><span class="sxs-lookup"><span data-stu-id="ce68d-111">This command will switch slot "sourceslot" slot with "destinationslot" for for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ce68d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce68d-112">PARAMETERS</span></span>

### <span data-ttu-id="ce68d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce68d-113">-DefaultProfile</span></span>
<span data-ttu-id="ce68d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce68d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="ce68d-115">-DestinationSlotName</span></span>
<span data-ttu-id="ce68d-116">Cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="ce68d-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce68d-117">-Name</span></span>
<span data-ttu-id="ce68d-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="ce68d-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="ce68d-119">-PreserveVnet</span></span>
<span data-ttu-id="ce68d-120">A vnet logikai értékének megőrzése</span><span class="sxs-lookup"><span data-stu-id="ce68d-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce68d-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce68d-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ce68d-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="ce68d-123">-SourceSlotName</span></span>
<span data-ttu-id="ce68d-124">Forrás bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="ce68d-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="ce68d-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="ce68d-126">Csere előzetes eljárással</span><span class="sxs-lookup"><span data-stu-id="ce68d-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ce68d-127">-WebApp</span></span>
<span data-ttu-id="ce68d-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="ce68d-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce68d-129">-Confirm</span></span>
<span data-ttu-id="ce68d-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce68d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce68d-131">-WhatIf</span></span>
<span data-ttu-id="ce68d-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce68d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce68d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce68d-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce68d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce68d-134">CommonParameters</span></span>
<span data-ttu-id="ce68d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce68d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce68d-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce68d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce68d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce68d-137">INPUTS</span></span>

### <span data-ttu-id="ce68d-138">Webhely</span><span class="sxs-lookup"><span data-stu-id="ce68d-138">Site</span></span>
<span data-ttu-id="ce68d-139">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ce68d-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ce68d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce68d-140">OUTPUTS</span></span>

## <span data-ttu-id="ce68d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce68d-141">NOTES</span></span>

## <span data-ttu-id="ce68d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce68d-142">RELATED LINKS</span></span>

