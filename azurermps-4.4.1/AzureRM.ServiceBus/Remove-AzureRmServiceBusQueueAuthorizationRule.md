---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494680"
---
# <span data-ttu-id="7941c-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7941c-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="7941c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7941c-102">SYNOPSIS</span></span>
<span data-ttu-id="7941c-103">Eltávolítja egy várólista engedélyezési szabályát a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="7941c-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7941c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7941c-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7941c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7941c-105">DESCRIPTION</span></span>
<span data-ttu-id="7941c-106">A **Remove-AzureRmServiceBusQueueAuthorizationRule** parancsmag eltávolítja egy várólista engedélyezési szabályát a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="7941c-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7941c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7941c-107">EXAMPLES</span></span>

### <span data-ttu-id="7941c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7941c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="7941c-109">Eltávolítja a várólista engedélyezési szabályát `SBAuthoRule1` `SB-Queue_exampl1` a névtérből `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7941c-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7941c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7941c-110">PARAMETERS</span></span>

### <span data-ttu-id="7941c-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7941c-111">-ResourceGroup</span></span>
<span data-ttu-id="7941c-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7941c-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7941c-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7941c-113">-Confirm</span></span>
<span data-ttu-id="7941c-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7941c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7941c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7941c-115">-WhatIf</span></span>
<span data-ttu-id="7941c-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7941c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7941c-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7941c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7941c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7941c-118">-DefaultProfile</span></span>
<span data-ttu-id="7941c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7941c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7941c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7941c-120">-Name</span></span>
<span data-ttu-id="7941c-121">A várólista AuthorizationRule neve.</span><span class="sxs-lookup"><span data-stu-id="7941c-121">Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7941c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7941c-122">-Namespace</span></span>
<span data-ttu-id="7941c-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="7941c-123">Namespace Name.</span></span>

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

### <span data-ttu-id="7941c-124">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="7941c-124">-Queue</span></span>
<span data-ttu-id="7941c-125">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="7941c-125">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7941c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7941c-126">CommonParameters</span></span>
<span data-ttu-id="7941c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7941c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7941c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7941c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7941c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7941c-129">INPUTS</span></span>

### <span data-ttu-id="7941c-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7941c-130">-ResourceGroup</span></span>
 <span data-ttu-id="7941c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7941c-131">System.String</span></span>

### <span data-ttu-id="7941c-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7941c-132">-NamespaceName</span></span>
 <span data-ttu-id="7941c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7941c-133">System.String</span></span>

### <span data-ttu-id="7941c-134">-QueueName</span><span class="sxs-lookup"><span data-stu-id="7941c-134">-QueueName</span></span>
 <span data-ttu-id="7941c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7941c-135">System.String</span></span>

### <span data-ttu-id="7941c-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7941c-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="7941c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7941c-137">System.String</span></span>

## <span data-ttu-id="7941c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7941c-138">OUTPUTS</span></span>

### <span data-ttu-id="7941c-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="7941c-139">System.Object</span></span>

## <span data-ttu-id="7941c-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7941c-140">NOTES</span></span>

## <span data-ttu-id="7941c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7941c-141">RELATED LINKS</span></span>

