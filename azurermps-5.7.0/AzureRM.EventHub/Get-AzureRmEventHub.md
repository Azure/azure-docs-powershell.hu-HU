---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495369"
---
# <span data-ttu-id="ce897-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="ce897-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="ce897-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce897-102">SYNOPSIS</span></span>
<span data-ttu-id="ce897-103">Beolvassa az egyetlen esemény központjának részleteit, vagy megkapja az esemény-hubok listáját.</span><span class="sxs-lookup"><span data-stu-id="ce897-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce897-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce897-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce897-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce897-105">DESCRIPTION</span></span>
<span data-ttu-id="ce897-106">A Get-AzureRmEventHub parancsmag az esemény központjának részleteit vagy az aktuális névtérben lévő összes esemény hubok listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ce897-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="ce897-107">Ha az esemény-hub neve meg van határozva, akkor az adott esemény egyetlen csomópontjának adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="ce897-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="ce897-108">Ha egy esemény-hub neve nincs megadva, a megadott névtérben lévő összes esemény-hubok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ce897-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="ce897-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ce897-109">EXAMPLES</span></span>

### <span data-ttu-id="ce897-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ce897-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ce897-111">Az esemény központi MyEventHubName részleteit számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="ce897-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="ce897-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ce897-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="ce897-113">A névtér MyNamespaceName az esemény-hubok listáját számítja ki \` \` .</span><span class="sxs-lookup"><span data-stu-id="ce897-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="ce897-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce897-114">PARAMETERS</span></span>

### <span data-ttu-id="ce897-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce897-115">-DefaultProfile</span></span>
<span data-ttu-id="ce897-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce897-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce897-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce897-117">-Name</span></span>
<span data-ttu-id="ce897-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="ce897-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce897-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ce897-119">-Namespace</span></span>
<span data-ttu-id="ce897-120">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ce897-120">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce897-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce897-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce897-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ce897-122">Resource Group Name</span></span>

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

### <span data-ttu-id="ce897-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce897-123">CommonParameters</span></span>
<span data-ttu-id="ce897-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce897-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ce897-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce897-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce897-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce897-126">INPUTS</span></span>

### <span data-ttu-id="ce897-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ce897-127">System.String</span></span>


## <span data-ttu-id="ce897-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce897-128">OUTPUTS</span></span>

### <span data-ttu-id="ce897-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes, Microsoft. Azure. commands. EventHub, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ce897-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="ce897-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce897-130">NOTES</span></span>

## <span data-ttu-id="ce897-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce897-131">RELATED LINKS</span></span>
