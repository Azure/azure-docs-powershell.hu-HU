---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: 621fb15d3a83b7c704e5828d6541ad9d4404875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501867"
---
# <span data-ttu-id="399f1-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="399f1-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="399f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="399f1-102">SYNOPSIS</span></span>
<span data-ttu-id="399f1-103">Az Azure Event Grid által támogatott témák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="399f1-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="399f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="399f1-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="399f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="399f1-105">DESCRIPTION</span></span>
<span data-ttu-id="399f1-106">Az Azure Event Grid által támogatott témakörök részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="399f1-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="399f1-107">Ha meg van adva egy témakör típusa, a program az adott témakör részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="399f1-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="399f1-108">Ha a téma típusa név nincs megadva, a program a témakör minden típusának részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="399f1-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="399f1-109">Ha a IncludeEventTypes meg van adva, az egyes témák által támogatott esemény típusokra vonatkozó információk szerepelnek a válaszban.</span><span class="sxs-lookup"><span data-stu-id="399f1-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="399f1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="399f1-110">EXAMPLES</span></span>

### <span data-ttu-id="399f1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="399f1-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="399f1-112">A témakör típusainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="399f1-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="399f1-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="399f1-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="399f1-114">Információt kap a StorageAccounts témakör típusáról.</span><span class="sxs-lookup"><span data-stu-id="399f1-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="399f1-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="399f1-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="399f1-116">Információt kap a StorageAccounts, például a StorageAccounts által támogatott esemény típusokról.</span><span class="sxs-lookup"><span data-stu-id="399f1-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="399f1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="399f1-117">PARAMETERS</span></span>

### <span data-ttu-id="399f1-118">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="399f1-118">-IncludeEventTypeData</span></span>
<span data-ttu-id="399f1-119">Ha meg van adva, a válasz a téma típusa által támogatott esemény típusait fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="399f1-119">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="399f1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="399f1-120">-Name</span></span>
<span data-ttu-id="399f1-121">EventGrid a téma típusa név.</span><span class="sxs-lookup"><span data-stu-id="399f1-121">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="399f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="399f1-122">-DefaultProfile</span></span>
<span data-ttu-id="399f1-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="399f1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="399f1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="399f1-124">CommonParameters</span></span>
<span data-ttu-id="399f1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="399f1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="399f1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="399f1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="399f1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="399f1-127">INPUTS</span></span>

### <span data-ttu-id="399f1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="399f1-128">System.String</span></span>
<span data-ttu-id="399f1-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="399f1-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="399f1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="399f1-130">OUTPUTS</span></span>

### <span data-ttu-id="399f1-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfoListInstance, Microsoft. Azure. commands. EventGrid, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="399f1-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="399f1-132">Microsoft. Azure. Command. EventGrid. models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="399f1-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="399f1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="399f1-133">NOTES</span></span>

## <span data-ttu-id="399f1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="399f1-134">RELATED LINKS</span></span>

