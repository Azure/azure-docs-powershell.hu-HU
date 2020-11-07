---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 13de3f05879234a0db1af34517d37172c2a5a6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680023"
---
# <span data-ttu-id="66032-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66032-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="66032-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66032-102">SYNOPSIS</span></span>
<span data-ttu-id="66032-103">Egy adott továbbítóügynök (Namespace/WcfRelay/HybridConnection) adott engedélyezési szabályának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="66032-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66032-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66032-104">SYNTAX</span></span>

### <span data-ttu-id="66032-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66032-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66032-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="66032-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66032-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="66032-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66032-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="66032-108">DESCRIPTION</span></span>
<span data-ttu-id="66032-109">A **Get-AzureRmRelayAuthorizationRule** parancsmag az adott továbbítóügynök (Namespace/WcfRelay/HybridConnection) megadott engedélyezési szabály leírását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="66032-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="66032-110">Példák</span><span class="sxs-lookup"><span data-stu-id="66032-110">EXAMPLES</span></span>

### <span data-ttu-id="66032-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="66032-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="66032-112">Adott névtérhez megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="66032-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="66032-113">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="66032-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="66032-114">Adott WcfRelay megadott engedélyezési szabály leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="66032-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="66032-115">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="66032-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="66032-116">Adott HybridConnection megadott engedélyezési szabály leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="66032-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="66032-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66032-117">PARAMETERS</span></span>

### <span data-ttu-id="66032-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66032-118">-DefaultProfile</span></span>
<span data-ttu-id="66032-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66032-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66032-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="66032-120">-HybridConnection</span></span>
<span data-ttu-id="66032-121">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="66032-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66032-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66032-122">-Name</span></span>
<span data-ttu-id="66032-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="66032-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66032-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="66032-124">-Namespace</span></span>
<span data-ttu-id="66032-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="66032-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66032-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66032-126">-ResourceGroupName</span></span>
<span data-ttu-id="66032-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="66032-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="66032-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="66032-128">-WcfRelay</span></span>
<span data-ttu-id="66032-129">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="66032-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66032-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66032-130">CommonParameters</span></span>
<span data-ttu-id="66032-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66032-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="66032-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66032-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66032-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66032-133">INPUTS</span></span>

### <span data-ttu-id="66032-134">System. String</span><span class="sxs-lookup"><span data-stu-id="66032-134">System.String</span></span>


## <span data-ttu-id="66032-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66032-135">OUTPUTS</span></span>

### <span data-ttu-id="66032-136">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="66032-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="66032-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66032-137">NOTES</span></span>

## <span data-ttu-id="66032-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66032-138">RELATED LINKS</span></span>
