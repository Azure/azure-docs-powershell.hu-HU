---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: e5a4886eef132f0e48c146fa70889dfa283489b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494345"
---
# <span data-ttu-id="eccbd-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eccbd-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="eccbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eccbd-102">SYNOPSIS</span></span>
<span data-ttu-id="eccbd-103">A megadott névtérre vagy-várólistára vagy-aliasra (GeoDR-konfigurációk) vonatkozó meghatározott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="eccbd-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 


[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eccbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eccbd-104">SYNTAX</span></span>

### <span data-ttu-id="eccbd-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eccbd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eccbd-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eccbd-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eccbd-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eccbd-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eccbd-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="eccbd-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eccbd-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="eccbd-109">DESCRIPTION</span></span>
<span data-ttu-id="eccbd-110">A **Get-AzureRmServiceBusAuthorizationRule** parancsmag a megadott engedélyezési szabály leírását adja meg a megadott névtérben vagy sorban, illetve az aliasban (GeoDR-konfigurációk).</span><span class="sxs-lookup"><span data-stu-id="eccbd-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="eccbd-111">Példák</span><span class="sxs-lookup"><span data-stu-id="eccbd-111">EXAMPLES</span></span>

### <span data-ttu-id="eccbd-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eccbd-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="eccbd-113">Adott névtérhez megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="eccbd-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="eccbd-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="eccbd-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="eccbd-115">Adott várólista megadott engedélyezési szabályának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="eccbd-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="eccbd-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="eccbd-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="eccbd-117">Adott témakörhöz megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="eccbd-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="eccbd-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="eccbd-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="eccbd-119">A megadott névtérhez és aliashoz megadott engedélyezési szabály leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="eccbd-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="eccbd-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eccbd-120">PARAMETERS</span></span>

### <span data-ttu-id="eccbd-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="eccbd-121">-AliasName</span></span>
<span data-ttu-id="eccbd-122">GeoDR-konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="eccbd-122">GeoDR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eccbd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eccbd-123">-DefaultProfile</span></span>
<span data-ttu-id="eccbd-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eccbd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eccbd-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eccbd-125">-Name</span></span>
<span data-ttu-id="eccbd-126">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="eccbd-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eccbd-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eccbd-127">-Namespace</span></span>
<span data-ttu-id="eccbd-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="eccbd-128">Namespace Name</span></span>

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

### <span data-ttu-id="eccbd-129">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="eccbd-129">-Queue</span></span>
<span data-ttu-id="eccbd-130">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="eccbd-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eccbd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eccbd-131">-ResourceGroupName</span></span>
<span data-ttu-id="eccbd-132">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="eccbd-132">Resource Group Name</span></span>

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

### <span data-ttu-id="eccbd-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="eccbd-133">-Topic</span></span>
<span data-ttu-id="eccbd-134">Téma neve</span><span class="sxs-lookup"><span data-stu-id="eccbd-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eccbd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eccbd-135">CommonParameters</span></span>
<span data-ttu-id="eccbd-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eccbd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eccbd-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eccbd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eccbd-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eccbd-138">INPUTS</span></span>

### <span data-ttu-id="eccbd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eccbd-139">System.String</span></span>


## <span data-ttu-id="eccbd-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eccbd-140">OUTPUTS</span></span>

### <span data-ttu-id="eccbd-141">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eccbd-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="eccbd-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eccbd-142">NOTES</span></span>

## <span data-ttu-id="eccbd-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eccbd-143">RELATED LINKS</span></span>
