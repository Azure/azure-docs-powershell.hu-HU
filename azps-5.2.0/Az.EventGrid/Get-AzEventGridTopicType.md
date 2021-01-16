---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338250"
---
# <span data-ttu-id="7d510-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="7d510-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="7d510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d510-102">SYNOPSIS</span></span>
<span data-ttu-id="7d510-103">Az Azure Event Grid által támogatott témakörtípusokról ad részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="7d510-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="7d510-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7d510-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d510-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7d510-105">DESCRIPTION</span></span>
<span data-ttu-id="7d510-106">Az Azure Event Grid által támogatott témakörök típusainak részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7d510-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="7d510-107">Ha egy témakörtípus neve meg van adva, a témakör típusának részleteit adja vissza a visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="7d510-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="7d510-108">Ha nincs megadva egy tématípus neve, az összes témakörtípusra vonatkozó részleteket adja vissza a visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="7d510-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="7d510-109">Ha az IncludeEventTypes érték meg van adva, az egyes témakörtípusok által támogatott eseménytípusokra vonatkozó információk szerepelnek a válaszban.</span><span class="sxs-lookup"><span data-stu-id="7d510-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="7d510-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7d510-110">EXAMPLES</span></span>

### <span data-ttu-id="7d510-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7d510-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="7d510-112">A témakörtípusok listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7d510-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="7d510-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7d510-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="7d510-114">Információkat kap a StorageAccounts témakör típusról.</span><span class="sxs-lookup"><span data-stu-id="7d510-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="7d510-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7d510-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="7d510-116">Információkat kap a StorageAccounts témakör típusról, beleértve a StorageAccounts által támogatott eseménytípusokat.</span><span class="sxs-lookup"><span data-stu-id="7d510-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="7d510-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d510-117">PARAMETERS</span></span>

### <span data-ttu-id="7d510-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d510-118">-DefaultProfile</span></span>
<span data-ttu-id="7d510-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7d510-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d510-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="7d510-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="7d510-121">Ha meg van adva, a válasz tartalmazza a témakörtípus által támogatott eseménytípusokat.</span><span class="sxs-lookup"><span data-stu-id="7d510-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="7d510-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7d510-122">-Name</span></span>
<span data-ttu-id="7d510-123">EventGrid-témakörtípus neve.</span><span class="sxs-lookup"><span data-stu-id="7d510-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="7d510-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d510-124">CommonParameters</span></span>
<span data-ttu-id="7d510-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d510-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d510-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d510-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d510-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d510-127">INPUTS</span></span>

### <span data-ttu-id="7d510-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7d510-128">System.String</span></span>

## <span data-ttu-id="7d510-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d510-129">OUTPUTS</span></span>

### <span data-ttu-id="7d510-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="7d510-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="7d510-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="7d510-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="7d510-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7d510-132">NOTES</span></span>

## <span data-ttu-id="7d510-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d510-133">RELATED LINKS</span></span>
