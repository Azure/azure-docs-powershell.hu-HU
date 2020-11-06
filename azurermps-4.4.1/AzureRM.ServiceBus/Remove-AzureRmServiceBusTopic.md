---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 356140c964280634f469dd9b9955adaf62130090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493355"
---
# <span data-ttu-id="5cf23-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="5cf23-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="5cf23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cf23-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf23-103">A megadott szolgáltatási busz névtérből eltávolítja a témakört.</span><span class="sxs-lookup"><span data-stu-id="5cf23-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cf23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cf23-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cf23-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cf23-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf23-106">A **Remove-AzureRmServiceBusTopic** parancsmag eltávolítja a témakört a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="5cf23-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5cf23-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5cf23-107">EXAMPLES</span></span>

### <span data-ttu-id="5cf23-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5cf23-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="5cf23-109">Eltávolítja a témakört `SB-Topic_exampl1` a névtérből `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="5cf23-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="5cf23-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cf23-110">PARAMETERS</span></span>

### <span data-ttu-id="5cf23-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5cf23-111">-Confirm</span></span>
<span data-ttu-id="5cf23-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5cf23-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf23-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf23-113">-WhatIf</span></span>
<span data-ttu-id="5cf23-114">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5cf23-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf23-115">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cf23-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf23-116">-DefaultProfile</span></span>
<span data-ttu-id="5cf23-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cf23-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cf23-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5cf23-118">-Name</span></span>
<span data-ttu-id="5cf23-119">A téma neve</span><span class="sxs-lookup"><span data-stu-id="5cf23-119">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf23-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5cf23-120">-Namespace</span></span>
<span data-ttu-id="5cf23-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="5cf23-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf23-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf23-122">-ResourceGroupName</span></span>
<span data-ttu-id="5cf23-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5cf23-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf23-124">CommonParameters</span></span>
<span data-ttu-id="5cf23-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cf23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf23-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf23-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf23-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cf23-127">INPUTS</span></span>

### <span data-ttu-id="5cf23-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5cf23-128">-ResourceGroup</span></span>
 <span data-ttu-id="5cf23-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf23-129">System.String</span></span>

### <span data-ttu-id="5cf23-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5cf23-130">-NamespaceName</span></span>
 <span data-ttu-id="5cf23-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf23-131">System.String</span></span>

### <span data-ttu-id="5cf23-132">-TopicName</span><span class="sxs-lookup"><span data-stu-id="5cf23-132">-TopicName</span></span>
 <span data-ttu-id="5cf23-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf23-133">System.String</span></span>

## <span data-ttu-id="5cf23-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cf23-134">OUTPUTS</span></span>

### <span data-ttu-id="5cf23-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5cf23-135">System.Object</span></span>

## <span data-ttu-id="5cf23-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cf23-136">NOTES</span></span>

## <span data-ttu-id="5cf23-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cf23-137">RELATED LINKS</span></span>

