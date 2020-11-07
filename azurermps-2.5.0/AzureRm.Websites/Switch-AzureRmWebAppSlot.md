---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9671c2041f767df5066353988eb633318289de47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848594"
---
# <span data-ttu-id="e664b-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e664b-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="e664b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e664b-102">SYNOPSIS</span></span>
<span data-ttu-id="e664b-103">Két bővítőhely cseréje webalkalmazással</span><span class="sxs-lookup"><span data-stu-id="e664b-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e664b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e664b-104">SYNTAX</span></span>

### <span data-ttu-id="e664b-105">S1</span><span class="sxs-lookup"><span data-stu-id="e664b-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e664b-106">S2</span><span class="sxs-lookup"><span data-stu-id="e664b-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e664b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e664b-107">DESCRIPTION</span></span>
<span data-ttu-id="e664b-108">A **kapcsoló – AzureRmWebAppSlot** két bővítőhelyet vált át az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="e664b-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="e664b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e664b-109">EXAMPLES</span></span>

### <span data-ttu-id="e664b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e664b-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="e664b-111">Ez a parancs a "sourceslot" bővítőhely "destinationslot" típusú, az erőforráscsoport alapértelmezett ContosoWebApp társított ""-webhelyre vált, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="e664b-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e664b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e664b-112">PARAMETERS</span></span>

### <span data-ttu-id="e664b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e664b-113">-DefaultProfile</span></span>
<span data-ttu-id="e664b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e664b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e664b-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="e664b-115">-DestinationSlotName</span></span>
<span data-ttu-id="e664b-116">Cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="e664b-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="e664b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e664b-117">-Name</span></span>
<span data-ttu-id="e664b-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e664b-118">WebApp Name</span></span>

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

### <span data-ttu-id="e664b-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="e664b-119">-PreserveVnet</span></span>
<span data-ttu-id="e664b-120">A vnet logikai értékének megőrzése</span><span class="sxs-lookup"><span data-stu-id="e664b-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="e664b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e664b-121">-ResourceGroupName</span></span>
<span data-ttu-id="e664b-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e664b-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e664b-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="e664b-123">-SourceSlotName</span></span>
<span data-ttu-id="e664b-124">Forrás bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="e664b-124">Source Slot Name</span></span>

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

### <span data-ttu-id="e664b-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="e664b-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="e664b-126">Csere előzetes eljárással</span><span class="sxs-lookup"><span data-stu-id="e664b-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="e664b-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e664b-127">-WebApp</span></span>
<span data-ttu-id="e664b-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="e664b-128">WebApp Object</span></span>

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

### <span data-ttu-id="e664b-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e664b-129">-Confirm</span></span>
<span data-ttu-id="e664b-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e664b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e664b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e664b-131">-WhatIf</span></span>
<span data-ttu-id="e664b-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e664b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e664b-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e664b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e664b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e664b-134">CommonParameters</span></span>
<span data-ttu-id="e664b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e664b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e664b-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e664b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e664b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e664b-137">INPUTS</span></span>

### <span data-ttu-id="e664b-138">Webhely</span><span class="sxs-lookup"><span data-stu-id="e664b-138">Site</span></span>
<span data-ttu-id="e664b-139">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e664b-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e664b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e664b-140">OUTPUTS</span></span>

## <span data-ttu-id="e664b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e664b-141">NOTES</span></span>

## <span data-ttu-id="e664b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e664b-142">RELATED LINKS</span></span>

