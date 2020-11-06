---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: cd3182a2a00f488dabd70a97d06693362068768c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502939"
---
# <span data-ttu-id="61922-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="61922-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="61922-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61922-102">SYNOPSIS</span></span>
<span data-ttu-id="61922-103">Az Azure Event Grid által támogatott témák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="61922-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61922-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61922-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61922-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61922-105">DESCRIPTION</span></span>
<span data-ttu-id="61922-106">Az Azure Event Grid által támogatott témakörök részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="61922-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="61922-107">Ha meg van adva egy témakör típusa, a program az adott témakör részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="61922-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="61922-108">Ha a téma típusa név nincs megadva, a program a témakör minden típusának részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="61922-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="61922-109">Ha a IncludeEventTypes meg van adva, az egyes témák által támogatott esemény típusokra vonatkozó információk szerepelnek a válaszban.</span><span class="sxs-lookup"><span data-stu-id="61922-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="61922-110">Példák</span><span class="sxs-lookup"><span data-stu-id="61922-110">EXAMPLES</span></span>

### <span data-ttu-id="61922-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="61922-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="61922-112">A témakör típusainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="61922-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="61922-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="61922-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="61922-114">Információt kap a StorageAccounts témakör típusáról.</span><span class="sxs-lookup"><span data-stu-id="61922-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="61922-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="61922-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="61922-116">Információt kap a StorageAccounts, például a StorageAccounts által támogatott esemény típusokról.</span><span class="sxs-lookup"><span data-stu-id="61922-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="61922-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61922-117">PARAMETERS</span></span>

### <span data-ttu-id="61922-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61922-118">-DefaultProfile</span></span>
<span data-ttu-id="61922-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="61922-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61922-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="61922-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="61922-121">Ha meg van adva, a válasz a téma típusa által támogatott esemény típusait fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="61922-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="61922-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61922-122">-Name</span></span>
<span data-ttu-id="61922-123">EventGrid a téma típusa név.</span><span class="sxs-lookup"><span data-stu-id="61922-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="61922-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61922-124">CommonParameters</span></span>
<span data-ttu-id="61922-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61922-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61922-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61922-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61922-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61922-127">INPUTS</span></span>

### <span data-ttu-id="61922-128">System. String</span><span class="sxs-lookup"><span data-stu-id="61922-128">System.String</span></span>

## <span data-ttu-id="61922-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61922-129">OUTPUTS</span></span>

### <span data-ttu-id="61922-130">Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="61922-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="61922-131">Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="61922-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="61922-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61922-132">NOTES</span></span>

## <span data-ttu-id="61922-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61922-133">RELATED LINKS</span></span>
