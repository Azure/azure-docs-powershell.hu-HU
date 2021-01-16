---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343710"
---
# <span data-ttu-id="e9387-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e9387-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e9387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9387-102">SYNOPSIS</span></span>
<span data-ttu-id="e9387-103">Egy adott névtérhez, várólistához, témakörhez vagy aliashoz (GeoDR-konfigurációk) megadott engedélyezési szabály leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="e9387-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="e9387-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9387-104">SYNTAX</span></span>

### <span data-ttu-id="e9387-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9387-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9387-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9387-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9387-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9387-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9387-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9387-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9387-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9387-109">DESCRIPTION</span></span>
<span data-ttu-id="e9387-110">A **Get-AzServiceBusAuthorizationRule** parancsmag megkapja a megadott engedélyezési szabály leírását a megadott Namespace vagy Queue or Topic or Alias (GeoDR Configurations) mezőben.</span><span class="sxs-lookup"><span data-stu-id="e9387-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="e9387-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9387-111">EXAMPLES</span></span>

### <span data-ttu-id="e9387-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e9387-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="e9387-113">Egy megadott névtér engedélyezési szabályának leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e9387-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="e9387-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e9387-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="e9387-115">Egy adott várólistához megadott engedélyezési szabály leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e9387-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="e9387-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="e9387-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="e9387-117">Egy adott témakör engedélyezési szabályának megadott leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e9387-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="e9387-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="e9387-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="e9387-119">Visszaadja egy megadott névtér és alias engedélyezési szabályának leírását.</span><span class="sxs-lookup"><span data-stu-id="e9387-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="e9387-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9387-120">PARAMETERS</span></span>

### <span data-ttu-id="e9387-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e9387-121">-AliasName</span></span>
<span data-ttu-id="e9387-122">GeoDR Configuration Name</span><span class="sxs-lookup"><span data-stu-id="e9387-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="e9387-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9387-123">-DefaultProfile</span></span>
<span data-ttu-id="e9387-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9387-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9387-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e9387-125">-Name</span></span>
<span data-ttu-id="e9387-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="e9387-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e9387-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e9387-127">-Namespace</span></span>
<span data-ttu-id="e9387-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="e9387-128">Namespace Name</span></span>

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

### <span data-ttu-id="e9387-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="e9387-129">-Queue</span></span>
<span data-ttu-id="e9387-130">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="e9387-130">Queue Name</span></span>

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

### <span data-ttu-id="e9387-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9387-131">-ResourceGroupName</span></span>
<span data-ttu-id="e9387-132">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e9387-132">Resource Group Name</span></span>

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

### <span data-ttu-id="e9387-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="e9387-133">-Topic</span></span>
<span data-ttu-id="e9387-134">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="e9387-134">Topic Name</span></span>

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

### <span data-ttu-id="e9387-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9387-135">CommonParameters</span></span>
<span data-ttu-id="e9387-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9387-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9387-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9387-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9387-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9387-138">INPUTS</span></span>

### <span data-ttu-id="e9387-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e9387-139">System.String</span></span>

## <span data-ttu-id="e9387-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9387-140">OUTPUTS</span></span>

### <span data-ttu-id="e9387-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e9387-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e9387-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9387-142">NOTES</span></span>

## <span data-ttu-id="e9387-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9387-143">RELATED LINKS</span></span>
