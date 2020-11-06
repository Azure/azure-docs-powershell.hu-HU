---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502727"
---
# <span data-ttu-id="d8c10-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="d8c10-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="d8c10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8c10-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c10-103">Beolvassa az esemény-hubok névterének részleteit, vagy az aktuális Azure-előfizetésből az összes esemény-hubok névterének listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="d8c10-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8c10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8c10-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="d8c10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8c10-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c10-106">A Get-AzureRmEventHubNamespace parancsmag az aktuális Azure-előfizetésben lévő adott esemény-hubok névterének részleteit vagy az összes esemény hubok névterét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d8c10-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="d8c10-107">Ha a névtér neve meg van határozva, az egyetlen esemény-hubok névtér részleteit adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="d8c10-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="d8c10-108">Ha a névtér neve nincs megadva, a program a névterek listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d8c10-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="d8c10-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d8c10-109">EXAMPLES</span></span>

### <span data-ttu-id="d8c10-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d8c10-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="d8c10-111">Az esemény-hubok névtér-MyNamespaceName részleteit kapja \` \` meg az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d8c10-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d8c10-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8c10-112">PARAMETERS</span></span>

### <span data-ttu-id="d8c10-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c10-113">-ResourceGroupName</span></span>
<span data-ttu-id="d8c10-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d8c10-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8c10-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d8c10-115">-Name</span></span>
<span data-ttu-id="d8c10-116">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="d8c10-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d8c10-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8c10-117">INPUTS</span></span>

### <span data-ttu-id="d8c10-118">System. String</span><span class="sxs-lookup"><span data-stu-id="d8c10-118">System.String</span></span>

## <span data-ttu-id="d8c10-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8c10-119">OUTPUTS</span></span>

### <span data-ttu-id="d8c10-120">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. NamespaceAttributes, Microsoft. Azure. commands. EventHub, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d8c10-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d8c10-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8c10-121">NOTES</span></span>

## <span data-ttu-id="d8c10-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8c10-122">RELATED LINKS</span></span>

