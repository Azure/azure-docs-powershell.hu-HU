---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187457"
---
# <span data-ttu-id="4e8de-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="4e8de-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="4e8de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e8de-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8de-103">Az Azure Event Grid által támogatott témák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4e8de-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="4e8de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e8de-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e8de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e8de-105">DESCRIPTION</span></span>
<span data-ttu-id="4e8de-106">Az Azure Event Grid által támogatott témakörök részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4e8de-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="4e8de-107">Ha meg van adva egy témakör típusa, a program az adott témakör részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="4e8de-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="4e8de-108">Ha a téma típusa név nincs megadva, a program a témakör minden típusának részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="4e8de-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="4e8de-109">Ha a IncludeEventTypes meg van adva, az egyes témák által támogatott esemény típusokra vonatkozó információk szerepelnek a válaszban.</span><span class="sxs-lookup"><span data-stu-id="4e8de-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="4e8de-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4e8de-110">EXAMPLES</span></span>

### <span data-ttu-id="4e8de-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4e8de-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="4e8de-112">A témakör típusainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="4e8de-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="4e8de-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4e8de-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="4e8de-114">Információt kap a StorageAccounts témakör típusáról.</span><span class="sxs-lookup"><span data-stu-id="4e8de-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="4e8de-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="4e8de-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="4e8de-116">Információt kap a StorageAccounts, például a StorageAccounts által támogatott esemény típusokról.</span><span class="sxs-lookup"><span data-stu-id="4e8de-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="4e8de-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e8de-117">PARAMETERS</span></span>

### <span data-ttu-id="4e8de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8de-118">-DefaultProfile</span></span>
<span data-ttu-id="4e8de-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4e8de-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e8de-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="4e8de-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="4e8de-121">Ha meg van adva, a válasz a téma típusa által támogatott esemény típusait fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="4e8de-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e8de-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e8de-122">-Name</span></span>
<span data-ttu-id="4e8de-123">EventGrid a téma típusa név.</span><span class="sxs-lookup"><span data-stu-id="4e8de-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e8de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8de-124">CommonParameters</span></span>
<span data-ttu-id="4e8de-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e8de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8de-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4e8de-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8de-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e8de-127">INPUTS</span></span>

### <span data-ttu-id="4e8de-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4e8de-128">System.String</span></span>

## <span data-ttu-id="4e8de-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e8de-129">OUTPUTS</span></span>

### <span data-ttu-id="4e8de-130">Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="4e8de-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="4e8de-131">Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="4e8de-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="4e8de-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e8de-132">NOTES</span></span>

## <span data-ttu-id="4e8de-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e8de-133">RELATED LINKS</span></span>