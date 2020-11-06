---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: f2d295d31b0112a2adf73e2e4be064164df8fbb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502419"
---
# <span data-ttu-id="6761a-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6761a-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="6761a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6761a-102">SYNOPSIS</span></span>
<span data-ttu-id="6761a-103">A megadott szolgáltatási busz névtérből eltávolítja a témakört.</span><span class="sxs-lookup"><span data-stu-id="6761a-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6761a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6761a-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6761a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6761a-105">DESCRIPTION</span></span>
<span data-ttu-id="6761a-106">A **Remove-AzureRmServiceBusTopic** parancsmag eltávolítja a témakört a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="6761a-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6761a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6761a-107">EXAMPLES</span></span>

### <span data-ttu-id="6761a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6761a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="6761a-109">Eltávolítja a témakört `SB-Topic_exampl1` a névtérből `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="6761a-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="6761a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6761a-110">PARAMETERS</span></span>

### <span data-ttu-id="6761a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6761a-111">-DefaultProfile</span></span>
<span data-ttu-id="6761a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6761a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6761a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6761a-113">-Name</span></span>
<span data-ttu-id="6761a-114">A téma neve</span><span class="sxs-lookup"><span data-stu-id="6761a-114">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6761a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6761a-115">-Namespace</span></span>
<span data-ttu-id="6761a-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="6761a-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6761a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6761a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6761a-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6761a-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6761a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6761a-119">-Confirm</span></span>
<span data-ttu-id="6761a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6761a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6761a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6761a-121">-WhatIf</span></span>
<span data-ttu-id="6761a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6761a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6761a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6761a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6761a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6761a-124">CommonParameters</span></span>
<span data-ttu-id="6761a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6761a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6761a-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6761a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6761a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6761a-127">INPUTS</span></span>

### <span data-ttu-id="6761a-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6761a-128">-ResourceGroup</span></span>
 <span data-ttu-id="6761a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6761a-129">System.String</span></span>

### <span data-ttu-id="6761a-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6761a-130">-NamespaceName</span></span>
 <span data-ttu-id="6761a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6761a-131">System.String</span></span>

### <span data-ttu-id="6761a-132">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6761a-132">-TopicName</span></span>
 <span data-ttu-id="6761a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6761a-133">System.String</span></span>

## <span data-ttu-id="6761a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6761a-134">OUTPUTS</span></span>

### <span data-ttu-id="6761a-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="6761a-135">System.Object</span></span>

## <span data-ttu-id="6761a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6761a-136">NOTES</span></span>

## <span data-ttu-id="6761a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6761a-137">RELATED LINKS</span></span>

