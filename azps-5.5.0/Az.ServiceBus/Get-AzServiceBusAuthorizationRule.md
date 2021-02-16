---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168915"
---
# <span data-ttu-id="fc5e5-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fc5e5-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="fc5e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5e5-103">Egy adott névtérhez, várólistához, témakörhez vagy aliashoz (GeoDR-konfigurációk) megadott engedélyezési szabály leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="fc5e5-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="fc5e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc5e5-104">SYNTAX</span></span>

### <span data-ttu-id="fc5e5-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc5e5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc5e5-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc5e5-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc5e5-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc5e5-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc5e5-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc5e5-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc5e5-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc5e5-109">DESCRIPTION</span></span>
<span data-ttu-id="fc5e5-110">A **Get-AzServiceBusAuthorizationRule** parancsmag megkapja a megadott engedélyezési szabály leírását a megadott Névtér vagy Várólistán, Illetve Témakör vagy Alias (GeoDR-konfigurációk) belül.</span><span class="sxs-lookup"><span data-stu-id="fc5e5-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="fc5e5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc5e5-111">EXAMPLES</span></span>

### <span data-ttu-id="fc5e5-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="fc5e5-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="fc5e5-113">Egy megadott névtér engedélyezési szabályának leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fc5e5-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="fc5e5-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="fc5e5-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="fc5e5-115">Egy adott várólistához megadott engedélyezési szabály leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fc5e5-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="fc5e5-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="fc5e5-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="fc5e5-117">Egy adott témakör engedélyezési szabályának megadott leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fc5e5-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="fc5e5-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="fc5e5-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="fc5e5-119">Egy megadott névtérhez és aliashoz megadott engedélyezési szabályleírást ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="fc5e5-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="fc5e5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc5e5-120">PARAMETERS</span></span>

### <span data-ttu-id="fc5e5-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="fc5e5-121">-AliasName</span></span>
<span data-ttu-id="fc5e5-122">GeoDR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="fc5e5-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="fc5e5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5e5-123">-DefaultProfile</span></span>
<span data-ttu-id="fc5e5-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc5e5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5e5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fc5e5-125">-Name</span></span>
<span data-ttu-id="fc5e5-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="fc5e5-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="fc5e5-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc5e5-127">-Namespace</span></span>
<span data-ttu-id="fc5e5-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="fc5e5-128">Namespace Name</span></span>

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

### <span data-ttu-id="fc5e5-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="fc5e5-129">-Queue</span></span>
<span data-ttu-id="fc5e5-130">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="fc5e5-130">Queue Name</span></span>

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

### <span data-ttu-id="fc5e5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5e5-131">-ResourceGroupName</span></span>
<span data-ttu-id="fc5e5-132">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fc5e5-132">Resource Group Name</span></span>

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

### <span data-ttu-id="fc5e5-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="fc5e5-133">-Topic</span></span>
<span data-ttu-id="fc5e5-134">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="fc5e5-134">Topic Name</span></span>

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

### <span data-ttu-id="fc5e5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5e5-135">CommonParameters</span></span>
<span data-ttu-id="fc5e5-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc5e5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5e5-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5e5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5e5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc5e5-138">INPUTS</span></span>

### <span data-ttu-id="fc5e5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fc5e5-139">System.String</span></span>

## <span data-ttu-id="fc5e5-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc5e5-140">OUTPUTS</span></span>

### <span data-ttu-id="fc5e5-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fc5e5-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="fc5e5-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc5e5-142">NOTES</span></span>

## <span data-ttu-id="fc5e5-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc5e5-143">RELATED LINKS</span></span>
