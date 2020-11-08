---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183590"
---
# <span data-ttu-id="32b43-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="32b43-101">Get-AzEventHub</span></span>

## <span data-ttu-id="32b43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32b43-102">SYNOPSIS</span></span>
<span data-ttu-id="32b43-103">Beolvassa az egyetlen esemény központjának részleteit, vagy megkapja az esemény-hubok listáját.</span><span class="sxs-lookup"><span data-stu-id="32b43-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="32b43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32b43-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32b43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32b43-105">DESCRIPTION</span></span>
<span data-ttu-id="32b43-106">A Get-AzEventHub parancsmag az esemény központjának részleteit vagy az aktuális névtérben lévő összes esemény hubok listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="32b43-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="32b43-107">Ha az esemény-hub neve meg van határozva, akkor az adott esemény egyetlen csomópontjának adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="32b43-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="32b43-108">Ha egy esemény-hub neve nincs megadva, a megadott névtérben lévő összes esemény-hubok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="32b43-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="32b43-109">Példák</span><span class="sxs-lookup"><span data-stu-id="32b43-109">EXAMPLES</span></span>

### <span data-ttu-id="32b43-110">Példa 1: megadott EventHub</span><span class="sxs-lookup"><span data-stu-id="32b43-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="32b43-111">Az esemény központi MyEventHubName részleteit számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="32b43-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="32b43-112">2. példa: a megadott névtér EventHub listája</span><span class="sxs-lookup"><span data-stu-id="32b43-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="32b43-113">A névtér MyNamespaceName az esemény-hubok listáját számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="32b43-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="32b43-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32b43-114">PARAMETERS</span></span>

### <span data-ttu-id="32b43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b43-115">-DefaultProfile</span></span>
<span data-ttu-id="32b43-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32b43-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b43-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="32b43-117">-MaxCount</span></span>
<span data-ttu-id="32b43-118">Adja meg a EventHubs maximális számát.</span><span class="sxs-lookup"><span data-stu-id="32b43-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="32b43-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="32b43-119">-Name</span></span>
<span data-ttu-id="32b43-120">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="32b43-120">EventHub Name</span></span>

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

### <span data-ttu-id="32b43-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="32b43-121">-Namespace</span></span>
<span data-ttu-id="32b43-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="32b43-122">Namespace Name</span></span>

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

### <span data-ttu-id="32b43-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b43-123">-ResourceGroupName</span></span>
<span data-ttu-id="32b43-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="32b43-124">Resource Group Name</span></span>

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

### <span data-ttu-id="32b43-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b43-125">CommonParameters</span></span>
<span data-ttu-id="32b43-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32b43-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b43-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b43-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b43-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32b43-128">INPUTS</span></span>

### <span data-ttu-id="32b43-129">System. String</span><span class="sxs-lookup"><span data-stu-id="32b43-129">System.String</span></span>

## <span data-ttu-id="32b43-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32b43-130">OUTPUTS</span></span>

### <span data-ttu-id="32b43-131">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="32b43-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="32b43-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32b43-132">NOTES</span></span>

## <span data-ttu-id="32b43-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32b43-133">RELATED LINKS</span></span>
