---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680566"
---
# <span data-ttu-id="6631e-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6631e-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="6631e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6631e-102">SYNOPSIS</span></span>
<span data-ttu-id="6631e-103">Beolvassa a Eventubs-névtér engedélyezési szabályának részleteit, vagy megkapja az engedélyezési szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="6631e-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6631e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6631e-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="6631e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6631e-105">DESCRIPTION</span></span>
<span data-ttu-id="6631e-106">A Get-AzureRmEventHubNamespaceAuthorizationRule parancsmag a megadott esemény-hubok névtér-engedélyezési szabályának adatait vagy a névtér-engedélyezési szabályok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="6631e-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="6631e-107">Ha az engedélyezési szabály neve meg van határozva, az egyetlen engedélyezési szabály részleteit adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6631e-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="6631e-108">Ha egy engedélyezési szabály neve nincs megadva, a rendszer a névtérben lévő összes engedélyezési szabály listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="6631e-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="6631e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6631e-109">EXAMPLES</span></span>

### <span data-ttu-id="6631e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6631e-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="6631e-111">Az \` MyAuthRuleName az \` esemény-hubok névtér- \` MyNamespaceName \` , az erőforráscsoport \` MyResourceGroupName tartalmazó \` engedélyezési szabály értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6631e-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6631e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="6631e-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="6631e-113">Az esemény hubok névtér-MyNamespaceName az RootManageSharedAccessKey alapértelmezett engedélyezési szabályát számítja \` \` ki \` \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6631e-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6631e-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="6631e-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="6631e-115">Az esemény-hubok névtér-MyNamespaceName minden engedélyezési szabályát visszaállítja \` \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6631e-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6631e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6631e-116">PARAMETERS</span></span>

### <span data-ttu-id="6631e-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="6631e-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="6631e-118">Az esemény-hubok névtér-engedélyezési szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="6631e-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6631e-119">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6631e-119">-NamespaceName</span></span>
<span data-ttu-id="6631e-120">Az esemény hubok névterének neve.</span><span class="sxs-lookup"><span data-stu-id="6631e-120">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6631e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6631e-121">-ResourceGroupName</span></span>
<span data-ttu-id="6631e-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6631e-122">Resource group name.</span></span>

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

## <span data-ttu-id="6631e-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6631e-123">INPUTS</span></span>

### <span data-ttu-id="6631e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6631e-124">System.String</span></span>

## <span data-ttu-id="6631e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6631e-125">OUTPUTS</span></span>

### <span data-ttu-id="6631e-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. EventHub, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6631e-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6631e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6631e-127">NOTES</span></span>

## <span data-ttu-id="6631e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6631e-128">RELATED LINKS</span></span>

