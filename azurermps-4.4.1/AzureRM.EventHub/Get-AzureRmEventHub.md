---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505040"
---
# <span data-ttu-id="8d083-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="8d083-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="8d083-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d083-102">SYNOPSIS</span></span>
<span data-ttu-id="8d083-103">Beolvassa az egyetlen esemény központjának részleteit, vagy megkapja az esemény-hubok listáját.</span><span class="sxs-lookup"><span data-stu-id="8d083-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d083-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d083-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="8d083-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d083-105">DESCRIPTION</span></span>
<span data-ttu-id="8d083-106">A Get-AzureRmEventHub parancsmag az esemény központjának részleteit vagy az aktuális névtérben lévő összes esemény hubok listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="8d083-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="8d083-107">Ha az esemény-hub neve meg van határozva, akkor az adott esemény egyetlen csomópontjának adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="8d083-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="8d083-108">Ha egy esemény-hub neve nincs megadva, a megadott névtérben lévő összes esemény-hubok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8d083-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="8d083-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8d083-109">EXAMPLES</span></span>

### <span data-ttu-id="8d083-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8d083-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="8d083-111">Az esemény központi MyEventHubName részleteit számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="8d083-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="8d083-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8d083-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="8d083-113">A névtér MyNamespaceName az esemény-hubok listáját számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="8d083-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="8d083-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d083-114">PARAMETERS</span></span>

### <span data-ttu-id="8d083-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d083-115">-ResourceGroupName</span></span>
<span data-ttu-id="8d083-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8d083-116">Resource group name.</span></span>

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

### <span data-ttu-id="8d083-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d083-117">-Name</span></span>
<span data-ttu-id="8d083-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="8d083-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d083-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8d083-119">-Namespace</span></span>
<span data-ttu-id="8d083-120">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="8d083-120">Namespace Name.</span></span>

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

## <span data-ttu-id="8d083-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d083-121">INPUTS</span></span>

### <span data-ttu-id="8d083-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8d083-122">System.String</span></span>

## <span data-ttu-id="8d083-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d083-123">OUTPUTS</span></span>

### <span data-ttu-id="8d083-124">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. EventHubAttributes, Microsoft. Azure. commands. EventHub, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8d083-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8d083-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d083-125">NOTES</span></span>

## <span data-ttu-id="8d083-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d083-126">RELATED LINKS</span></span>

