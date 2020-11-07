---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 52788c012a7da6013e58df924d1eda0a3aa5afcb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835057"
---
# <span data-ttu-id="cefd2-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="cefd2-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="cefd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cefd2-102">SYNOPSIS</span></span>
<span data-ttu-id="cefd2-103">Új tevékenység-naplózási riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="cefd2-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="cefd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cefd2-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cefd2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cefd2-105">DESCRIPTION</span></span>
<span data-ttu-id="cefd2-106">A **New-AzActivityLogAlertCondition** parancsmag új tevékenység-naplózási riasztási feltétel objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="cefd2-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="cefd2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cefd2-107">EXAMPLES</span></span>

### <span data-ttu-id="cefd2-108">Példa 1: új tevékenység napló riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="cefd2-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="cefd2-109">Ez a parancs létrehoz egy új tevékenység napló riasztási feltétel objektumot a memóriában.</span><span class="sxs-lookup"><span data-stu-id="cefd2-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="cefd2-110">**Megjegyzés** : Ha ezt a parancsmagot a Set-AzActivityLogAlert legalább egy olyan objektummal együtt használja, amelyet paraméterként adott meg, a mezőnek egyenlőnek kell lennie a "kategória" értékkel.</span><span class="sxs-lookup"><span data-stu-id="cefd2-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="cefd2-111">Máskülönben a backend egy 400 (BadRequest.) válaszol.</span><span class="sxs-lookup"><span data-stu-id="cefd2-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="cefd2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cefd2-112">PARAMETERS</span></span>

### <span data-ttu-id="cefd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefd2-113">-DefaultProfile</span></span>
<span data-ttu-id="cefd2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cefd2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cefd2-115">-Egyenlő</span><span class="sxs-lookup"><span data-stu-id="cefd2-115">-Equal</span></span>
<span data-ttu-id="cefd2-116">A leveles feltétel egyenlő tulajdonságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cefd2-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="cefd2-117">-Mező</span><span class="sxs-lookup"><span data-stu-id="cefd2-117">-Field</span></span>
<span data-ttu-id="cefd2-118">A feltétel mezőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cefd2-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="cefd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefd2-119">CommonParameters</span></span>
<span data-ttu-id="cefd2-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cefd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefd2-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cefd2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefd2-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cefd2-122">INPUTS</span></span>

### <span data-ttu-id="cefd2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cefd2-123">System.String</span></span>

## <span data-ttu-id="cefd2-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cefd2-124">OUTPUTS</span></span>

### <span data-ttu-id="cefd2-125">Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="cefd2-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="cefd2-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cefd2-126">NOTES</span></span>

## <span data-ttu-id="cefd2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cefd2-127">RELATED LINKS</span></span>

[<span data-ttu-id="cefd2-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cefd2-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="cefd2-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cefd2-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="cefd2-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cefd2-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="cefd2-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cefd2-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="cefd2-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cefd2-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="cefd2-133">Új – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="cefd2-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
