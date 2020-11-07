---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: 662c2b5ed487a13c557e85709ed7b850a28acb2e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666499"
---
# <span data-ttu-id="ce59c-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="ce59c-101">Get-AzEventHub</span></span>

## <span data-ttu-id="ce59c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce59c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce59c-103">Beolvassa az egyetlen esemény központjának részleteit, vagy megkapja az esemény-hubok listáját.</span><span class="sxs-lookup"><span data-stu-id="ce59c-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="ce59c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce59c-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce59c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce59c-105">DESCRIPTION</span></span>
<span data-ttu-id="ce59c-106">A Get-AzEventHub parancsmag az esemény központjának részleteit vagy az aktuális névtérben lévő összes esemény hubok listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ce59c-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="ce59c-107">Ha az esemény-hub neve meg van határozva, akkor az adott esemény egyetlen csomópontjának adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="ce59c-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="ce59c-108">Ha egy esemény-hub neve nincs megadva, a megadott névtérben lévő összes esemény-hubok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ce59c-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="ce59c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ce59c-109">EXAMPLES</span></span>

### <span data-ttu-id="ce59c-110">Példa 1 – megadott EventHub</span><span class="sxs-lookup"><span data-stu-id="ce59c-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ce59c-111">Az esemény központi MyEventHubName részleteit számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="ce59c-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="ce59c-112">Példa 2 – a megadott névtér EventHub listája</span><span class="sxs-lookup"><span data-stu-id="ce59c-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="ce59c-113">A névtér MyNamespaceName az esemény-hubok listáját számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="ce59c-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="ce59c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce59c-114">PARAMETERS</span></span>

### <span data-ttu-id="ce59c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce59c-115">-DefaultProfile</span></span>
<span data-ttu-id="ce59c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce59c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce59c-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ce59c-117">-MaxCount</span></span>
<span data-ttu-id="ce59c-118">Adja meg a EventHubs maximális számát.</span><span class="sxs-lookup"><span data-stu-id="ce59c-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="ce59c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce59c-119">-Name</span></span>
<span data-ttu-id="ce59c-120">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="ce59c-120">EventHub Name</span></span>

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

### <span data-ttu-id="ce59c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ce59c-121">-Namespace</span></span>
<span data-ttu-id="ce59c-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ce59c-122">Namespace Name</span></span>

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

### <span data-ttu-id="ce59c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce59c-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce59c-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ce59c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ce59c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce59c-125">CommonParameters</span></span>
<span data-ttu-id="ce59c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce59c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce59c-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce59c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce59c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce59c-128">INPUTS</span></span>

### <span data-ttu-id="ce59c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ce59c-129">System.String</span></span>

## <span data-ttu-id="ce59c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce59c-130">OUTPUTS</span></span>

### <span data-ttu-id="ce59c-131">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ce59c-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="ce59c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce59c-132">NOTES</span></span>

## <span data-ttu-id="ce59c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce59c-133">RELATED LINKS</span></span>
