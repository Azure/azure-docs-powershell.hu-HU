---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 4932445406e19cbc05f5e2680871a03ae6f40f60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012985"
---
# <span data-ttu-id="9472e-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9472e-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="9472e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9472e-102">SYNOPSIS</span></span>
<span data-ttu-id="9472e-103">Új tevékenység-naplózási riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="9472e-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="9472e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9472e-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9472e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9472e-105">DESCRIPTION</span></span>
<span data-ttu-id="9472e-106">A **New-AzActivityLogAlertCondition** parancsmag új tevékenység-naplózási riasztási feltétel objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="9472e-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="9472e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9472e-107">EXAMPLES</span></span>

### <span data-ttu-id="9472e-108">Példa 1: új tevékenység napló riasztási feltétel objektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="9472e-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="9472e-109">Ez a parancs létrehoz egy új tevékenység napló riasztási feltétel objektumot a memóriában.</span><span class="sxs-lookup"><span data-stu-id="9472e-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="9472e-110">**Megjegyzés** : Ha ezt a parancsmagot a Set-AzActivityLogAlert legalább egy olyan objektummal együtt használja, amelyet paraméterként adott meg, a mezőnek egyenlőnek kell lennie a "kategória" értékkel.</span><span class="sxs-lookup"><span data-stu-id="9472e-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="9472e-111">Máskülönben a backend egy 400 (BadRequest.) válaszol.</span><span class="sxs-lookup"><span data-stu-id="9472e-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="9472e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9472e-112">PARAMETERS</span></span>

### <span data-ttu-id="9472e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9472e-113">-DefaultProfile</span></span>
<span data-ttu-id="9472e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9472e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9472e-115">-Egyenlő</span><span class="sxs-lookup"><span data-stu-id="9472e-115">-Equal</span></span>
<span data-ttu-id="9472e-116">A leveles feltétel egyenlő tulajdonságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9472e-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="9472e-117">-Mező</span><span class="sxs-lookup"><span data-stu-id="9472e-117">-Field</span></span>
<span data-ttu-id="9472e-118">A feltétel mezőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9472e-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="9472e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9472e-119">CommonParameters</span></span>
<span data-ttu-id="9472e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9472e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9472e-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9472e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9472e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9472e-122">INPUTS</span></span>

### <span data-ttu-id="9472e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9472e-123">System.String</span></span>

## <span data-ttu-id="9472e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9472e-124">OUTPUTS</span></span>

### <span data-ttu-id="9472e-125">Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="9472e-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="9472e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9472e-126">NOTES</span></span>

## <span data-ttu-id="9472e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9472e-127">RELATED LINKS</span></span>

[<span data-ttu-id="9472e-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9472e-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="9472e-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9472e-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="9472e-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9472e-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="9472e-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9472e-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="9472e-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9472e-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="9472e-133">Új – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="9472e-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
