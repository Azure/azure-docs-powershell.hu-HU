---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209566"
---
# <span data-ttu-id="8d5c1-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="8d5c1-101">Get-AzEventHub</span></span>

## <span data-ttu-id="8d5c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5c1-103">Lekérte egyetlen eseményközpont adatait, vagy lekérte az Eseményközpontok listáját.</span><span class="sxs-lookup"><span data-stu-id="8d5c1-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="8d5c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d5c1-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d5c1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d5c1-105">DESCRIPTION</span></span>
<span data-ttu-id="8d5c1-106">A Get-AzEventHub parancsmag vagy az Eseményközpont adatait, vagy az aktuális névtér összes eseményközpontját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8d5c1-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="8d5c1-107">Ha az Eseményközpont neve meg van téve, a visszaadott érték egyetlen eseményközpont adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8d5c1-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="8d5c1-108">Ha nem adja meg az Eseményközpont nevét, a megadott névtér összes eseményközpontja megjelenik.</span><span class="sxs-lookup"><span data-stu-id="8d5c1-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="8d5c1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d5c1-109">EXAMPLES</span></span>

### <span data-ttu-id="8d5c1-110">1. példa: megadott EventHub</span><span class="sxs-lookup"><span data-stu-id="8d5c1-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="8d5c1-111">A \` MyEventHubName eseményközpont adatait adja eredményül. \`</span><span class="sxs-lookup"><span data-stu-id="8d5c1-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="8d5c1-112">2. példa: Az EventHub listája a megadott Névtérben</span><span class="sxs-lookup"><span data-stu-id="8d5c1-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="8d5c1-113">A MyNamespaceName névterében található eseményközpontok listáját \` adja \` eredményül.</span><span class="sxs-lookup"><span data-stu-id="8d5c1-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="8d5c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d5c1-114">PARAMETERS</span></span>

### <span data-ttu-id="8d5c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5c1-115">-DefaultProfile</span></span>
<span data-ttu-id="8d5c1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d5c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d5c1-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8d5c1-117">-MaxCount</span></span>
<span data-ttu-id="8d5c1-118">Határozza meg, hogy legfeljebb hány EventHubot kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="8d5c1-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="8d5c1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8d5c1-119">-Name</span></span>
<span data-ttu-id="8d5c1-120">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="8d5c1-120">EventHub Name</span></span>

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

### <span data-ttu-id="8d5c1-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8d5c1-121">-Namespace</span></span>
<span data-ttu-id="8d5c1-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="8d5c1-122">Namespace Name</span></span>

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

### <span data-ttu-id="8d5c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d5c1-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8d5c1-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8d5c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5c1-125">CommonParameters</span></span>
<span data-ttu-id="8d5c1-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5c1-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5c1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5c1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d5c1-128">INPUTS</span></span>

### <span data-ttu-id="8d5c1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8d5c1-129">System.String</span></span>

## <span data-ttu-id="8d5c1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d5c1-130">OUTPUTS</span></span>

### <span data-ttu-id="8d5c1-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8d5c1-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="8d5c1-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d5c1-132">NOTES</span></span>

## <span data-ttu-id="8d5c1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d5c1-133">RELATED LINKS</span></span>
