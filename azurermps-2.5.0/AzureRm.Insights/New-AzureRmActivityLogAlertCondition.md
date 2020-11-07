---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
ms.openlocfilehash: a7ad8616bf2afc79d049384c1f20002ff6d6aa4a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848289"
---
# <span data-ttu-id="e1ab3-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e1ab3-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="e1ab3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ab3-103">Új tevékenység-naplózási riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="e1ab3-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ab3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1ab3-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ab3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ab3-106">A **New-AzureRmActivityLogAlertCondition** parancsmag új tevékenység-naplózási riasztási feltétel objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="e1ab3-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="e1ab3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ab3-108">Példa 1: új tevékenység napló riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="e1ab3-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="e1ab3-109">Ez a parancs létrehoz egy új tevékenység napló riasztási feltétel objektumot a memóriában.</span><span class="sxs-lookup"><span data-stu-id="e1ab3-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="e1ab3-110">**Megjegyzés** : Ha ezt a parancsmagot a Set-AzureRmActivityLogAlert legalább egy olyan objektummal együtt használja, amelyet paraméterként adott meg, a mezőnek egyenlőnek kell lennie a "kategória" értékkel.</span><span class="sxs-lookup"><span data-stu-id="e1ab3-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="e1ab3-111">Máskülönben a backend egy 400 (BadRequest.) válaszol.</span><span class="sxs-lookup"><span data-stu-id="e1ab3-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="e1ab3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1ab3-112">PARAMETERS</span></span>

### <span data-ttu-id="e1ab3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ab3-113">-DefaultProfile</span></span>
<span data-ttu-id="e1ab3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e1ab3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1ab3-115">-Egyenlő</span><span class="sxs-lookup"><span data-stu-id="e1ab3-115">-Equal</span></span>
<span data-ttu-id="e1ab3-116">A leveles feltétel egyenlő tulajdonságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1ab3-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="e1ab3-117">-Mező</span><span class="sxs-lookup"><span data-stu-id="e1ab3-117">-Field</span></span>
<span data-ttu-id="e1ab3-118">A feltétel mezőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1ab3-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="e1ab3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ab3-119">CommonParameters</span></span>
<span data-ttu-id="e1ab3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1ab3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ab3-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ab3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ab3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1ab3-122">INPUTS</span></span>

### <span data-ttu-id="e1ab3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ab3-123">System.String</span></span>

## <span data-ttu-id="e1ab3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1ab3-124">OUTPUTS</span></span>

### <span data-ttu-id="e1ab3-125">Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="e1ab3-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="e1ab3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1ab3-126">NOTES</span></span>

## <span data-ttu-id="e1ab3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1ab3-127">RELATED LINKS</span></span>

[<span data-ttu-id="e1ab3-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1ab3-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e1ab3-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1ab3-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e1ab3-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1ab3-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e1ab3-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1ab3-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e1ab3-132">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1ab3-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e1ab3-133">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e1ab3-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
