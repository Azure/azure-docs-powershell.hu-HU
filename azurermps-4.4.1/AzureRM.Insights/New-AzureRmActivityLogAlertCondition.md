---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 058f828037ad546ea5ed66aaadeef579c4908930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680538"
---
# <span data-ttu-id="90fc9-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="90fc9-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="90fc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="90fc9-103">Új tevékenység-naplózási riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="90fc9-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90fc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90fc9-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90fc9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="90fc9-106">A **New-AzureRmActivityLogAlertCondition** parancsmag új tevékenység-naplózási riasztási feltétel objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="90fc9-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="90fc9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90fc9-107">EXAMPLES</span></span>

### <span data-ttu-id="90fc9-108">Példa 1: új tevékenység napló riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="90fc9-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="90fc9-109">Ez a parancs létrehoz egy új tevékenység napló riasztási feltétel objektumot a memóriában.</span><span class="sxs-lookup"><span data-stu-id="90fc9-109">This command creates a new activity log alert condition object in memory.</span></span>

<span data-ttu-id="90fc9-110">**Megjegyzés** : Ha ezt a parancsmagot a Set-AzureRmActivityLogAlert legalább egy olyan objektummal együtt használja, amelyet paraméterként adott meg, a mezőnek egyenlőnek kell lennie a "kategória" értékkel.</span><span class="sxs-lookup"><span data-stu-id="90fc9-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="90fc9-111">Máskülönben a backend egy 400 (BadRequest.) válaszol.</span><span class="sxs-lookup"><span data-stu-id="90fc9-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="90fc9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90fc9-112">PARAMETERS</span></span>

### <span data-ttu-id="90fc9-113">-Mező</span><span class="sxs-lookup"><span data-stu-id="90fc9-113">-Field</span></span>
<span data-ttu-id="90fc9-114">A feltétel mezőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90fc9-114">Specifies the field for the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90fc9-115">-Egyenlő</span><span class="sxs-lookup"><span data-stu-id="90fc9-115">-Equal</span></span>
<span data-ttu-id="90fc9-116">A leveles feltétel egyenlő tulajdonságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="90fc9-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90fc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90fc9-117">-DefaultProfile</span></span>
<span data-ttu-id="90fc9-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90fc9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90fc9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90fc9-119">CommonParameters</span></span>
<span data-ttu-id="90fc9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90fc9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90fc9-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90fc9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90fc9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90fc9-122">INPUTS</span></span>

## <span data-ttu-id="90fc9-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90fc9-123">OUTPUTS</span></span>

### <span data-ttu-id="90fc9-124">Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="90fc9-124">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="90fc9-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90fc9-125">NOTES</span></span>

## <span data-ttu-id="90fc9-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90fc9-126">RELATED LINKS</span></span>

[<span data-ttu-id="90fc9-127">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90fc9-127">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="90fc9-128">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90fc9-128">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="90fc9-129">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90fc9-129">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="90fc9-130">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90fc9-130">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="90fc9-131">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90fc9-131">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="90fc9-132">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="90fc9-132">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
