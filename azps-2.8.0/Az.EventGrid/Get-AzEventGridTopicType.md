---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 7fc2777f4ab7f64aea4accb22d30f7df54c1476a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666528"
---
# <span data-ttu-id="3a659-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="3a659-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="3a659-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a659-102">SYNOPSIS</span></span>
<span data-ttu-id="3a659-103">Az Azure Event Grid által támogatott témák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a659-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="3a659-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a659-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a659-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a659-105">DESCRIPTION</span></span>
<span data-ttu-id="3a659-106">Az Azure Event Grid által támogatott témakörök részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3a659-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="3a659-107">Ha meg van adva egy témakör típusa, a program az adott témakör részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="3a659-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="3a659-108">Ha a téma típusa név nincs megadva, a program a témakör minden típusának részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="3a659-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="3a659-109">Ha a IncludeEventTypes meg van adva, az egyes témák által támogatott esemény típusokra vonatkozó információk szerepelnek a válaszban.</span><span class="sxs-lookup"><span data-stu-id="3a659-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="3a659-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3a659-110">EXAMPLES</span></span>

### <span data-ttu-id="3a659-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3a659-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="3a659-112">A témakör típusainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="3a659-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="3a659-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3a659-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="3a659-114">Információt kap a StorageAccounts témakör típusáról.</span><span class="sxs-lookup"><span data-stu-id="3a659-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="3a659-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="3a659-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="3a659-116">Információt kap a StorageAccounts, például a StorageAccounts által támogatott esemény típusokról.</span><span class="sxs-lookup"><span data-stu-id="3a659-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="3a659-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a659-117">PARAMETERS</span></span>

### <span data-ttu-id="3a659-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a659-118">-DefaultProfile</span></span>
<span data-ttu-id="3a659-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3a659-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a659-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="3a659-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="3a659-121">Ha meg van adva, a válasz a téma típusa által támogatott esemény típusait fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3a659-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="3a659-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a659-122">-Name</span></span>
<span data-ttu-id="3a659-123">EventGrid a téma típusa név.</span><span class="sxs-lookup"><span data-stu-id="3a659-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a659-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a659-124">CommonParameters</span></span>
<span data-ttu-id="3a659-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a659-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a659-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a659-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a659-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a659-127">INPUTS</span></span>

### <span data-ttu-id="3a659-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3a659-128">System.String</span></span>

## <span data-ttu-id="3a659-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a659-129">OUTPUTS</span></span>

### <span data-ttu-id="3a659-130">Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="3a659-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="3a659-131">Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="3a659-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="3a659-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a659-132">NOTES</span></span>

## <span data-ttu-id="3a659-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a659-133">RELATED LINKS</span></span>
