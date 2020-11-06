---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505008"
---
# <span data-ttu-id="74ef3-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="74ef3-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="74ef3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="74ef3-103">Új elsődleges vagy másodlagos kulcs létrehozása az engedélyezési szabályhoz a megadott esemény-hubok névtérben.</span><span class="sxs-lookup"><span data-stu-id="74ef3-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74ef3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74ef3-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="74ef3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="74ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="74ef3-106">Az New-AzureRmEventHubNamespaceKey parancsmag újra létrehozta a megadott engedélyezési szabály elsődleges vagy másodlagos kulcsát a megadott esemény-hubok névtérben.</span><span class="sxs-lookup"><span data-stu-id="74ef3-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="74ef3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="74ef3-107">EXAMPLES</span></span>

### <span data-ttu-id="74ef3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="74ef3-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="74ef3-109">Újragenerálja az elsődleges kulcsot az \` MyAuthRuleName az \` esemény-hubok névtér- \` MyNamespaceName, az \` erőforráscsoport- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="74ef3-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="74ef3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74ef3-110">PARAMETERS</span></span>

### <span data-ttu-id="74ef3-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="74ef3-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="74ef3-112">Engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="74ef3-112">Authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ef3-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="74ef3-113">-NamespaceName</span></span>
<span data-ttu-id="74ef3-114">Az esemény hubok névterének neve.</span><span class="sxs-lookup"><span data-stu-id="74ef3-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="74ef3-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="74ef3-115">-RegenerateKeys</span></span>
<span data-ttu-id="74ef3-116">Kulcs a regenerálódni: \` PrimaryKey \` vagy \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="74ef3-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ef3-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="74ef3-117">-ResourceGroup</span></span>
<span data-ttu-id="74ef3-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="74ef3-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="74ef3-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74ef3-119">-Confirm</span></span>
<span data-ttu-id="74ef3-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74ef3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ef3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ef3-121">-WhatIf</span></span>
<span data-ttu-id="74ef3-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74ef3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74ef3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74ef3-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="74ef3-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74ef3-124">INPUTS</span></span>

### <span data-ttu-id="74ef3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="74ef3-125">System.String</span></span>

## <span data-ttu-id="74ef3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74ef3-126">OUTPUTS</span></span>

### <span data-ttu-id="74ef3-127">Microsoft. Azure. Command. EventHub. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="74ef3-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="74ef3-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74ef3-128">NOTES</span></span>

## <span data-ttu-id="74ef3-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74ef3-129">RELATED LINKS</span></span>

