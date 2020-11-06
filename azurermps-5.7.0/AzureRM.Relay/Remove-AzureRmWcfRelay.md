---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 02949f3a16c9a259e645a035ce3e762db9582024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494389"
---
# <span data-ttu-id="9ed36-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="9ed36-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="9ed36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ed36-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed36-103">Eltávolítja a WcfRelay a megadott továbbítási névtérből.</span><span class="sxs-lookup"><span data-stu-id="9ed36-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ed36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ed36-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed36-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ed36-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed36-106">A **Remove-AzureRmWcfRelay** parancsmag eltávolítja a WcfRelay a megadott továbbító névtérből.</span><span class="sxs-lookup"><span data-stu-id="9ed36-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="9ed36-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ed36-107">EXAMPLES</span></span>

### <span data-ttu-id="9ed36-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ed36-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="9ed36-109">Eltávolítja a WcfRelay `TestWCFRelay1` a névtérből `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="9ed36-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="9ed36-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ed36-110">PARAMETERS</span></span>

### <span data-ttu-id="9ed36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed36-111">-DefaultProfile</span></span>
<span data-ttu-id="9ed36-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ed36-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ed36-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ed36-113">-Name</span></span>
<span data-ttu-id="9ed36-114">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="9ed36-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed36-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9ed36-115">-Namespace</span></span>
<span data-ttu-id="9ed36-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="9ed36-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed36-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed36-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ed36-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9ed36-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed36-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ed36-119">-Confirm</span></span>
<span data-ttu-id="9ed36-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ed36-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed36-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed36-121">-WhatIf</span></span>
<span data-ttu-id="9ed36-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ed36-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ed36-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ed36-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed36-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed36-124">CommonParameters</span></span>
<span data-ttu-id="9ed36-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ed36-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed36-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed36-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed36-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ed36-127">INPUTS</span></span>

### <span data-ttu-id="9ed36-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed36-128">-ResourceGroupName</span></span>
 <span data-ttu-id="9ed36-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed36-129">System.String</span></span>
 

### <span data-ttu-id="9ed36-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9ed36-130">-Namespace</span></span>
 <span data-ttu-id="9ed36-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed36-131">System.String</span></span>
 

### <span data-ttu-id="9ed36-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ed36-132">-Name</span></span>
 <span data-ttu-id="9ed36-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed36-133">System.String</span></span>

## <span data-ttu-id="9ed36-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ed36-134">OUTPUTS</span></span>

### <span data-ttu-id="9ed36-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="9ed36-135">System.Object</span></span>

## <span data-ttu-id="9ed36-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ed36-136">NOTES</span></span>

## <span data-ttu-id="9ed36-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ed36-137">RELATED LINKS</span></span>

