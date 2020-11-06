---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505036"
---
# <span data-ttu-id="06138-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="06138-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="06138-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06138-102">SYNOPSIS</span></span>
<span data-ttu-id="06138-103">Egy engedélyezési szabály részleteit kapja meg, vagy megkapja az engedélyezési szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="06138-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06138-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06138-104">SYNTAX</span></span>

### <span data-ttu-id="06138-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06138-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="06138-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="06138-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="06138-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="06138-107">DESCRIPTION</span></span>
<span data-ttu-id="06138-108">A Get-AzureRmEventHubAuthorizationRule parancsmag egy engedélyezési szabály részleteit vagy egy adott esemény központhoz tartozó összes engedélyezési szabály listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="06138-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="06138-109">Ha egy engedélyezési szabály neve meg van határozva, az adott egyetlen engedélyezési szabály részleteit adja vissza a függvény.</span><span class="sxs-lookup"><span data-stu-id="06138-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="06138-110">Ha egy engedélyezési szabály neve nem jelenik meg, akkor a megadott esemény központjának minden engedélyezési szabályát a program visszaadja.</span><span class="sxs-lookup"><span data-stu-id="06138-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="06138-111">Példák</span><span class="sxs-lookup"><span data-stu-id="06138-111">EXAMPLES</span></span>

### <span data-ttu-id="06138-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06138-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="06138-113">Az \` MyAuthRuleName az \` esemény központi \` MyEventHubName kapja \` , amelyet a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="06138-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="06138-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="06138-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="06138-115">Beolvassa az összes engedélyezési szabály listáját az esemény központi \` MyEventHubName \` , amelyet a névtér \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="06138-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="06138-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06138-116">PARAMETERS</span></span>

### <span data-ttu-id="06138-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06138-117">-ResourceGroupName</span></span>
<span data-ttu-id="06138-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="06138-118">Resource group name.</span></span>

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

### <span data-ttu-id="06138-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="06138-119">-Eventhub</span></span>
<span data-ttu-id="06138-120">Eventhub neve</span><span class="sxs-lookup"><span data-stu-id="06138-120">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06138-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06138-121">-Name</span></span>
<span data-ttu-id="06138-122">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="06138-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06138-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="06138-123">-Namespace</span></span>
<span data-ttu-id="06138-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="06138-124">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="06138-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06138-125">INPUTS</span></span>

### <span data-ttu-id="06138-126">System. String</span><span class="sxs-lookup"><span data-stu-id="06138-126">System.String</span></span>

## <span data-ttu-id="06138-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06138-127">OUTPUTS</span></span>

### <span data-ttu-id="06138-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. EventHub, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="06138-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="06138-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06138-129">NOTES</span></span>

## <span data-ttu-id="06138-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06138-130">RELATED LINKS</span></span>

