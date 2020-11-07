---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: 6ae26d1d5061989ac93756812cf48494e9101978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672942"
---
# <span data-ttu-id="e1bd6-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="e1bd6-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="e1bd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bd6-103">Beolvassa az egyetlen esemény központjának részleteit, vagy megkapja az esemény-hubok listáját.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1bd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1bd6-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1bd6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1bd6-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bd6-106">A Get-AzureRmEventHub parancsmag az esemény központjának részleteit vagy az aktuális névtérben lévő összes esemény hubok listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="e1bd6-107">Ha az esemény-hub neve meg van határozva, akkor az adott esemény egyetlen csomópontjának adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="e1bd6-108">Ha egy esemény-hub neve nincs megadva, a megadott névtérben lévő összes esemény-hubok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="e1bd6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e1bd6-109">EXAMPLES</span></span>

### <span data-ttu-id="e1bd6-110">Példa 1 – megadott EventHub</span><span class="sxs-lookup"><span data-stu-id="e1bd6-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="e1bd6-111">Az esemény központi MyEventHubName részleteit számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="e1bd6-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="e1bd6-112">Példa 2 – a megadott névtér EventHub listája</span><span class="sxs-lookup"><span data-stu-id="e1bd6-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="e1bd6-113">A névtér MyNamespaceName az esemény-hubok listáját számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="e1bd6-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="e1bd6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1bd6-114">PARAMETERS</span></span>

### <span data-ttu-id="e1bd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bd6-115">-DefaultProfile</span></span>
<span data-ttu-id="e1bd6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1bd6-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e1bd6-117">-MaxCount</span></span>
<span data-ttu-id="e1bd6-118">Adja meg a EventHubs maximális számát.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bd6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1bd6-119">-Name</span></span>
<span data-ttu-id="e1bd6-120">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="e1bd6-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bd6-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e1bd6-121">-Namespace</span></span>
<span data-ttu-id="e1bd6-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="e1bd6-122">Namespace Name</span></span>

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

### <span data-ttu-id="e1bd6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bd6-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1bd6-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e1bd6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e1bd6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bd6-125">CommonParameters</span></span>
<span data-ttu-id="e1bd6-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1bd6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bd6-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1bd6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bd6-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1bd6-128">INPUTS</span></span>

### <span data-ttu-id="e1bd6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e1bd6-129">System.String</span></span>

## <span data-ttu-id="e1bd6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1bd6-130">OUTPUTS</span></span>

### <span data-ttu-id="e1bd6-131">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e1bd6-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="e1bd6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1bd6-132">NOTES</span></span>

## <span data-ttu-id="e1bd6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1bd6-133">RELATED LINKS</span></span>
