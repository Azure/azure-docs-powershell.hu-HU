---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494682"
---
# <span data-ttu-id="8c5dd-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="8c5dd-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="8c5dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="8c5dd-103">Eltávolítja a névteret a megadott erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="8c5dd-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c5dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c5dd-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c5dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c5dd-105">DESCRIPTION</span></span>
<span data-ttu-id="8c5dd-106">A **Remove-AzureRmServiceBusNamespace** parancsmag eltávolítja a névteret a megadott erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="8c5dd-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="8c5dd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8c5dd-107">EXAMPLES</span></span>

### <span data-ttu-id="8c5dd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8c5dd-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="8c5dd-109">Eltávolítja a szervizsor névterét `SB-Example1` a megadott erőforráscsoport közül `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="8c5dd-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="8c5dd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c5dd-110">PARAMETERS</span></span>

### <span data-ttu-id="8c5dd-111">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8c5dd-111">-NamespaceName</span></span>
<span data-ttu-id="8c5dd-112">A szolgáltatás Buszjának névtér neve.</span><span class="sxs-lookup"><span data-stu-id="8c5dd-112">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="8c5dd-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c5dd-113">-ResourceGroup</span></span>
<span data-ttu-id="8c5dd-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8c5dd-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="8c5dd-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c5dd-115">-Confirm</span></span>
<span data-ttu-id="8c5dd-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c5dd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c5dd-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c5dd-117">-WhatIf</span></span>
<span data-ttu-id="8c5dd-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c5dd-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c5dd-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c5dd-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c5dd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c5dd-120">CommonParameters</span></span>
<span data-ttu-id="8c5dd-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c5dd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c5dd-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c5dd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c5dd-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c5dd-123">INPUTS</span></span>

### <span data-ttu-id="8c5dd-124">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c5dd-124">-ResourceGroup</span></span>
 <span data-ttu-id="8c5dd-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8c5dd-125">System.String</span></span>

### <span data-ttu-id="8c5dd-126">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8c5dd-126">-NamespaceName</span></span>
 <span data-ttu-id="8c5dd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8c5dd-127">System.String</span></span>

## <span data-ttu-id="8c5dd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c5dd-128">OUTPUTS</span></span>

### <span data-ttu-id="8c5dd-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="8c5dd-129">System.Object</span></span>

## <span data-ttu-id="8c5dd-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c5dd-130">NOTES</span></span>

## <span data-ttu-id="8c5dd-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c5dd-131">RELATED LINKS</span></span>

