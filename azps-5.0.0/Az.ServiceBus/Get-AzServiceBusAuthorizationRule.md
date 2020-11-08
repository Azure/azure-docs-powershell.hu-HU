---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185687"
---
# <span data-ttu-id="f4afd-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f4afd-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="f4afd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4afd-102">SYNOPSIS</span></span>
<span data-ttu-id="f4afd-103">A megadott névtérre vagy-várólistára vagy-aliasra (GeoDR-konfigurációk) vonatkozó meghatározott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4afd-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="f4afd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4afd-104">SYNTAX</span></span>

### <span data-ttu-id="f4afd-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4afd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4afd-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4afd-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4afd-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4afd-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4afd-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4afd-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4afd-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4afd-109">DESCRIPTION</span></span>
<span data-ttu-id="f4afd-110">A **Get-AzServiceBusAuthorizationRule** parancsmag a megadott engedélyezési szabály leírását adja meg a megadott névtérben vagy sorban, illetve az aliasban (GeoDR-konfigurációk).</span><span class="sxs-lookup"><span data-stu-id="f4afd-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="f4afd-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f4afd-111">EXAMPLES</span></span>

### <span data-ttu-id="f4afd-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4afd-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f4afd-113">Adott névtérhez megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4afd-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="f4afd-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="f4afd-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f4afd-115">Adott várólista megadott engedélyezési szabályának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4afd-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="f4afd-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="f4afd-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f4afd-117">Adott témakörhöz megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4afd-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="f4afd-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="f4afd-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="f4afd-119">A megadott névtérhez és aliashoz megadott engedélyezési szabály leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f4afd-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="f4afd-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4afd-120">PARAMETERS</span></span>

### <span data-ttu-id="f4afd-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="f4afd-121">-AliasName</span></span>
<span data-ttu-id="f4afd-122">GeoDR-konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="f4afd-122">GeoDR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4afd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4afd-123">-DefaultProfile</span></span>
<span data-ttu-id="f4afd-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4afd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4afd-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4afd-125">-Name</span></span>
<span data-ttu-id="f4afd-126">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="f4afd-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f4afd-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f4afd-127">-Namespace</span></span>
<span data-ttu-id="f4afd-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f4afd-128">Namespace Name</span></span>

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

### <span data-ttu-id="f4afd-129">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="f4afd-129">-Queue</span></span>
<span data-ttu-id="f4afd-130">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="f4afd-130">Queue Name</span></span>

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

### <span data-ttu-id="f4afd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4afd-131">-ResourceGroupName</span></span>
<span data-ttu-id="f4afd-132">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f4afd-132">Resource Group Name</span></span>

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

### <span data-ttu-id="f4afd-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="f4afd-133">-Topic</span></span>
<span data-ttu-id="f4afd-134">Téma neve</span><span class="sxs-lookup"><span data-stu-id="f4afd-134">Topic Name</span></span>

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

### <span data-ttu-id="f4afd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4afd-135">CommonParameters</span></span>
<span data-ttu-id="f4afd-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4afd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4afd-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4afd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4afd-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4afd-138">INPUTS</span></span>

### <span data-ttu-id="f4afd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f4afd-139">System.String</span></span>

## <span data-ttu-id="f4afd-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4afd-140">OUTPUTS</span></span>

### <span data-ttu-id="f4afd-141">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f4afd-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f4afd-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4afd-142">NOTES</span></span>

## <span data-ttu-id="f4afd-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4afd-143">RELATED LINKS</span></span>
