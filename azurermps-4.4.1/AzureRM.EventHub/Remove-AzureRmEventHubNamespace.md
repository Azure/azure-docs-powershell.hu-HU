---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500047"
---
# <span data-ttu-id="f4de9-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f4de9-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="f4de9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4de9-102">SYNOPSIS</span></span>
<span data-ttu-id="f4de9-103">Eltávolítja a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="f4de9-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4de9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4de9-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f4de9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4de9-105">DESCRIPTION</span></span>
<span data-ttu-id="f4de9-106">A Remove-AzureRmEventHubNamespace parancsmag eltávolítja és törli a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="f4de9-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="f4de9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4de9-107">EXAMPLES</span></span>

### <span data-ttu-id="f4de9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4de9-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="f4de9-109">Eltávolítja az esemény-hubok \` névtér \` -MyNamespaceName az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f4de9-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f4de9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4de9-110">PARAMETERS</span></span>

### <span data-ttu-id="f4de9-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4de9-111">-ResourceGroupName</span></span>
<span data-ttu-id="f4de9-112">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f4de9-112">Resource group name.</span></span>

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

### <span data-ttu-id="f4de9-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4de9-113">-Confirm</span></span>
<span data-ttu-id="f4de9-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4de9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4de9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4de9-115">-WhatIf</span></span>
<span data-ttu-id="f4de9-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4de9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4de9-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4de9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4de9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4de9-118">-Name</span></span>
<span data-ttu-id="f4de9-119">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="f4de9-119">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="f4de9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4de9-120">INPUTS</span></span>

### <span data-ttu-id="f4de9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f4de9-121">System.String</span></span>

## <span data-ttu-id="f4de9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4de9-122">OUTPUTS</span></span>

### <span data-ttu-id="f4de9-123">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="f4de9-123">System.Object</span></span>

## <span data-ttu-id="f4de9-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4de9-124">NOTES</span></span>

## <span data-ttu-id="f4de9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4de9-125">RELATED LINKS</span></span>

