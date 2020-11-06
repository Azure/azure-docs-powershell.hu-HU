---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 28c6bf4d463331755121e8a1ea14bf7f93407017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498808"
---
# <span data-ttu-id="a7a1c-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a7a1c-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="a7a1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a1c-103">Eltávolítja a várólistát a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="a7a1c-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7a1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7a1c-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a1c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a1c-106">A **Remove-AzureRmServiceBusQueue** parancsmag eltávolítja a várólistát a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="a7a1c-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a7a1c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a7a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a1c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a7a1c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="a7a1c-109">Eltávolítja a várólistát `SB-Queue_exampl1` a névtérből `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="a7a1c-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="a7a1c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="a7a1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a1c-111">-DefaultProfile</span></span>
<span data-ttu-id="a7a1c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7a1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a1c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7a1c-113">-Name</span></span>
<span data-ttu-id="a7a1c-114">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="a7a1c-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a1c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a7a1c-115">-Namespace</span></span>
<span data-ttu-id="a7a1c-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a7a1c-116">Namespace Name.</span></span>

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

### <span data-ttu-id="a7a1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7a1c-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a7a1c-118">The name of the resource group</span></span>

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

### <span data-ttu-id="a7a1c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a7a1c-119">-Confirm</span></span>
<span data-ttu-id="a7a1c-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a7a1c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a1c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a1c-121">-WhatIf</span></span>
<span data-ttu-id="a7a1c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a7a1c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a1c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7a1c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a1c-124">CommonParameters</span></span>
<span data-ttu-id="a7a1c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7a1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a1c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a1c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a1c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7a1c-127">INPUTS</span></span>

### <span data-ttu-id="a7a1c-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a7a1c-128">-ResourceGroup</span></span>
 <span data-ttu-id="a7a1c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a1c-129">System.String</span></span>

### <span data-ttu-id="a7a1c-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a7a1c-130">-NamespaceName</span></span>
 <span data-ttu-id="a7a1c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a1c-131">System.String</span></span>

### <span data-ttu-id="a7a1c-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="a7a1c-132">-QueueName</span></span>
 <span data-ttu-id="a7a1c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a1c-133">System.String</span></span>

## <span data-ttu-id="a7a1c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7a1c-134">OUTPUTS</span></span>

### <span data-ttu-id="a7a1c-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a7a1c-135">System.Object</span></span>

## <span data-ttu-id="a7a1c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7a1c-136">NOTES</span></span>

## <span data-ttu-id="a7a1c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7a1c-137">RELATED LINKS</span></span>

