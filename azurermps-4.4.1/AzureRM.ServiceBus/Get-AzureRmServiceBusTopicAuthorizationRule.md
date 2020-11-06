---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503204"
---
# <span data-ttu-id="f89f7-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f89f7-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="f89f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f89f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f89f7-103">Az adott témakörhöz tartozó meghatározott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f89f7-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f89f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f89f7-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f89f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f89f7-105">DESCRIPTION</span></span>
<span data-ttu-id="f89f7-106">A **Get-AzureRmServiceBusTopicAuthorizationRule** parancsmag a megadott szolgáltatási buszról a megadott engedélyezési szabály leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="f89f7-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="f89f7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f89f7-107">EXAMPLES</span></span>

### <span data-ttu-id="f89f7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f89f7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="f89f7-109">A megadott témakörhöz tartozó meghatározott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f89f7-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="f89f7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f89f7-110">PARAMETERS</span></span>

### <span data-ttu-id="f89f7-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f89f7-111">-ResourceGroup</span></span>
<span data-ttu-id="f89f7-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f89f7-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f89f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89f7-113">-DefaultProfile</span></span>
<span data-ttu-id="f89f7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f89f7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f89f7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f89f7-115">-Name</span></span>
<span data-ttu-id="f89f7-116">A AuthorizationRule témakör neve</span><span class="sxs-lookup"><span data-stu-id="f89f7-116">Topic AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89f7-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f89f7-117">-Namespace</span></span>
<span data-ttu-id="f89f7-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f89f7-118">Namespace Name.</span></span>

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

### <span data-ttu-id="f89f7-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="f89f7-119">-Topic</span></span>
<span data-ttu-id="f89f7-120">A téma neve</span><span class="sxs-lookup"><span data-stu-id="f89f7-120">Topic Name.</span></span>

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

### <span data-ttu-id="f89f7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89f7-121">CommonParameters</span></span>
<span data-ttu-id="f89f7-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f89f7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89f7-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89f7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89f7-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f89f7-124">INPUTS</span></span>

### <span data-ttu-id="f89f7-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f89f7-125">-ResourceGroup</span></span>
 <span data-ttu-id="f89f7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f89f7-126">System.String</span></span>
 

### <span data-ttu-id="f89f7-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f89f7-127">-NamespaceName</span></span>
 <span data-ttu-id="f89f7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f89f7-128">System.String</span></span>
 

### <span data-ttu-id="f89f7-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="f89f7-129">-TopicName</span></span>
 <span data-ttu-id="f89f7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f89f7-130">System.String</span></span>
 

### <span data-ttu-id="f89f7-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f89f7-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f89f7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f89f7-132">System.String</span></span>

## <span data-ttu-id="f89f7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f89f7-133">OUTPUTS</span></span>

### <span data-ttu-id="f89f7-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f89f7-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f89f7-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 típus: Microsoft. ServiceBus/AuthorizationRules név: SBTopicAuthoRule1 hely: West US Tags: Rights: {figyelj, küldés}</span><span class="sxs-lookup"><span data-stu-id="f89f7-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f89f7-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f89f7-136">NOTES</span></span>

## <span data-ttu-id="f89f7-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f89f7-137">RELATED LINKS</span></span>

