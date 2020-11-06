---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 287a0b82c9236841b613ac52a7a07ccf8adb4811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494675"
---
# <span data-ttu-id="4eccf-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4eccf-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="4eccf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4eccf-102">SYNOPSIS</span></span>
<span data-ttu-id="4eccf-103">Egy adott előfizetés speficied szabályát távolítja el.</span><span class="sxs-lookup"><span data-stu-id="4eccf-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eccf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4eccf-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eccf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4eccf-105">DESCRIPTION</span></span>
<span data-ttu-id="4eccf-106">A **Remove-AzureRmServiceBusRule** parancsmag eltávolítja az adott témakörhöz tartozó előfizetés szabályát.</span><span class="sxs-lookup"><span data-stu-id="4eccf-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="4eccf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4eccf-107">EXAMPLES</span></span>

### <span data-ttu-id="4eccf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4eccf-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="4eccf-109">Eltávolítja a `SBRule` megadott témakör előfizetési szabályát `SBSubscription` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="4eccf-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="4eccf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4eccf-110">PARAMETERS</span></span>

### <span data-ttu-id="4eccf-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4eccf-111">-Confirm</span></span>
<span data-ttu-id="4eccf-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4eccf-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eccf-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4eccf-113">-Name</span></span>
<span data-ttu-id="4eccf-114">Szabály neve.</span><span class="sxs-lookup"><span data-stu-id="4eccf-114">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eccf-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4eccf-115">-Namespace</span></span>
<span data-ttu-id="4eccf-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="4eccf-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eccf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eccf-117">-ResourceGroupName</span></span>
<span data-ttu-id="4eccf-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4eccf-118">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eccf-119">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="4eccf-119">-Subscription</span></span>
<span data-ttu-id="4eccf-120">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="4eccf-120">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eccf-121">-Topic</span><span class="sxs-lookup"><span data-stu-id="4eccf-121">-Topic</span></span>
<span data-ttu-id="4eccf-122">A téma neve</span><span class="sxs-lookup"><span data-stu-id="4eccf-122">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eccf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eccf-123">-WhatIf</span></span>
<span data-ttu-id="4eccf-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4eccf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eccf-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4eccf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eccf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eccf-126">-DefaultProfile</span></span>
<span data-ttu-id="4eccf-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4eccf-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eccf-128">-Force</span><span class="sxs-lookup"><span data-stu-id="4eccf-128">-Force</span></span>
<span data-ttu-id="4eccf-129">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4eccf-129">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eccf-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eccf-130">-PassThru</span></span>
<span data-ttu-id="4eccf-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4eccf-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eccf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eccf-132">CommonParameters</span></span>
<span data-ttu-id="4eccf-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4eccf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eccf-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eccf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eccf-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eccf-135">INPUTS</span></span>

### <span data-ttu-id="4eccf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4eccf-136">System.String</span></span>

## <span data-ttu-id="4eccf-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eccf-137">OUTPUTS</span></span>

### <span data-ttu-id="4eccf-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4eccf-138">System.Boolean</span></span>

## <span data-ttu-id="4eccf-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4eccf-139">NOTES</span></span>

## <span data-ttu-id="4eccf-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4eccf-140">RELATED LINKS</span></span>

