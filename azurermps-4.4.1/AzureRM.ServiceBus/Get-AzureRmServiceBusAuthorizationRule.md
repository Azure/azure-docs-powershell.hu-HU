---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504731"
---
# <span data-ttu-id="5c330-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5c330-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="5c330-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c330-102">SYNOPSIS</span></span>
<span data-ttu-id="5c330-103">A megadott névtérhez, várólistához vagy témakörhöz tartozó meghatározott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c330-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c330-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c330-104">SYNTAX</span></span>

### <span data-ttu-id="5c330-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c330-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c330-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c330-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c330-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c330-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c330-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c330-108">DESCRIPTION</span></span>
<span data-ttu-id="5c330-109">A **Get-AzureRmServiceBusAuthorizationRule** parancsmag az adott névtérben vagy várólistában vagy témakörben megadott engedélyezési szabály leírását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5c330-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="5c330-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5c330-110">EXAMPLES</span></span>

### <span data-ttu-id="5c330-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5c330-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="5c330-112">Adott névtérhez megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c330-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="5c330-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5c330-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="5c330-114">Adott várólista megadott engedélyezési szabályának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c330-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="5c330-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="5c330-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="5c330-116">Adott témakörhöz megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c330-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="5c330-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c330-117">PARAMETERS</span></span>

### <span data-ttu-id="5c330-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5c330-118">-Name</span></span>
<span data-ttu-id="5c330-119">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="5c330-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c330-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5c330-120">-Namespace</span></span>
<span data-ttu-id="5c330-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="5c330-121">Namespace Name.</span></span>

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

### <span data-ttu-id="5c330-122">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="5c330-122">-Queue</span></span>
<span data-ttu-id="5c330-123">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="5c330-123">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c330-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c330-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c330-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5c330-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c330-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="5c330-126">-Topic</span></span>
<span data-ttu-id="5c330-127">A téma neve</span><span class="sxs-lookup"><span data-stu-id="5c330-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c330-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c330-128">-DefaultProfile</span></span>
<span data-ttu-id="5c330-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c330-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c330-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c330-130">CommonParameters</span></span>
<span data-ttu-id="5c330-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c330-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c330-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c330-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c330-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c330-133">INPUTS</span></span>

### <span data-ttu-id="5c330-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5c330-134">System.String</span></span>

## <span data-ttu-id="5c330-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c330-135">OUTPUTS</span></span>

### <span data-ttu-id="5c330-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.4.2.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5c330-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5c330-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c330-137">NOTES</span></span>
## <span data-ttu-id="5c330-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c330-138">RELATED LINKS</span></span>

## <span data-ttu-id="5c330-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c330-139">RELATED LINKS</span></span>

