---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: 9522fe6925ac266ff87f3ba6b3540980d91c160f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680845"
---
# <span data-ttu-id="a69db-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a69db-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="a69db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a69db-102">SYNOPSIS</span></span>
<span data-ttu-id="a69db-103">Két bővítőhely cseréje webalkalmazással</span><span class="sxs-lookup"><span data-stu-id="a69db-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a69db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a69db-104">SYNTAX</span></span>

### <span data-ttu-id="a69db-105">S1</span><span class="sxs-lookup"><span data-stu-id="a69db-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a69db-106">S2</span><span class="sxs-lookup"><span data-stu-id="a69db-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a69db-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a69db-107">DESCRIPTION</span></span>
<span data-ttu-id="a69db-108">A **kapcsoló – AzureRmWebAppSlot** két bővítőhelyet vált át az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="a69db-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="a69db-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a69db-109">EXAMPLES</span></span>

### <span data-ttu-id="a69db-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a69db-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a69db-111">Ez a parancs a "sourceslot" bővítőhely "destinationslot" típusú, az erőforráscsoport alapértelmezett ContosoWebApp társított ""-webhelyre vált, a web-WestUS</span><span class="sxs-lookup"><span data-stu-id="a69db-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="a69db-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a69db-112">PARAMETERS</span></span>

### <span data-ttu-id="a69db-113">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="a69db-113">-DestinationSlotName</span></span>
<span data-ttu-id="a69db-114">Cél tárolóhelyének neve</span><span class="sxs-lookup"><span data-stu-id="a69db-114">Destination Slot Name</span></span>

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

### <span data-ttu-id="a69db-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a69db-115">-Name</span></span>
<span data-ttu-id="a69db-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="a69db-116">WebApp Name</span></span>

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

### <span data-ttu-id="a69db-117">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="a69db-117">-PreserveVnet</span></span>
<span data-ttu-id="a69db-118">A vnet logikai értékének megőrzése</span><span class="sxs-lookup"><span data-stu-id="a69db-118">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="a69db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69db-119">-ResourceGroupName</span></span>
<span data-ttu-id="a69db-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a69db-120">Resource Group Name</span></span>

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

### <span data-ttu-id="a69db-121">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="a69db-121">-SourceSlotName</span></span>
<span data-ttu-id="a69db-122">Forrás bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="a69db-122">Source Slot Name</span></span>

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

### <span data-ttu-id="a69db-123">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="a69db-123">-SwapWithPreviewAction</span></span>
<span data-ttu-id="a69db-124">Csere előzetes eljárással</span><span class="sxs-lookup"><span data-stu-id="a69db-124">Swap With Preview Action</span></span>

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

### <span data-ttu-id="a69db-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a69db-125">-WebApp</span></span>
<span data-ttu-id="a69db-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="a69db-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a69db-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a69db-127">-Confirm</span></span>
<span data-ttu-id="a69db-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a69db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a69db-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a69db-129">-WhatIf</span></span>
<span data-ttu-id="a69db-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a69db-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a69db-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a69db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a69db-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69db-132">-DefaultProfile</span></span>
<span data-ttu-id="a69db-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a69db-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69db-134">CommonParameters</span></span>
<span data-ttu-id="a69db-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a69db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69db-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a69db-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69db-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a69db-137">INPUTS</span></span>

### <span data-ttu-id="a69db-138">Webhely</span><span class="sxs-lookup"><span data-stu-id="a69db-138">Site</span></span>
<span data-ttu-id="a69db-139">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a69db-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a69db-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a69db-140">OUTPUTS</span></span>

## <span data-ttu-id="a69db-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a69db-141">NOTES</span></span>

## <span data-ttu-id="a69db-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a69db-142">RELATED LINKS</span></span>

