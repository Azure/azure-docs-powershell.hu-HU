---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 85cf08b0ade67042c4aa4c4c5ff3253b6af9f2ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380658"
---
# <span data-ttu-id="098be-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="098be-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="098be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098be-102">SYNOPSIS</span></span>
<span data-ttu-id="098be-103">Létrehoz egy új tevékenységnapló-riasztási feltételobjektumot a memóriában.</span><span class="sxs-lookup"><span data-stu-id="098be-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="098be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="098be-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="098be-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="098be-105">DESCRIPTION</span></span>
<span data-ttu-id="098be-106">A **New-AzActivityLogAlertCondition parancsmag** új tevékenységnapló-riasztási feltételobjektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="098be-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="098be-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="098be-107">EXAMPLES</span></span>

### <span data-ttu-id="098be-108">1. példa: Új tevékenységnapló-riasztási feltételobjektum létrehozása a memóriában.</span><span class="sxs-lookup"><span data-stu-id="098be-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="098be-109">Ez a parancs új tevékenységnapló-riasztási feltételobjektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="098be-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="098be-110">**MEGJEGYZÉS:** Ha ezt a parancsmagot a [Set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) paraméterként átadott objektumok közül legalább egyhez használja, a mezőnek "Kategória" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="098be-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="098be-111">Ellenkező esetben a háttéren egy 400-as (BadRequest)-es válasz lesz.</span><span class="sxs-lookup"><span data-stu-id="098be-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="098be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="098be-112">PARAMETERS</span></span>

### <span data-ttu-id="098be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098be-113">-DefaultProfile</span></span>
<span data-ttu-id="098be-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="098be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="098be-115">-Equal</span><span class="sxs-lookup"><span data-stu-id="098be-115">-Equal</span></span>
<span data-ttu-id="098be-116">A levél feltételének egyenlő tulajdonságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="098be-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="098be-117">-Mező</span><span class="sxs-lookup"><span data-stu-id="098be-117">-Field</span></span>
<span data-ttu-id="098be-118">A feltétel mezőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="098be-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="098be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098be-119">CommonParameters</span></span>
<span data-ttu-id="098be-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098be-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="098be-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098be-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="098be-122">INPUTS</span></span>

### <span data-ttu-id="098be-123">System.String</span><span class="sxs-lookup"><span data-stu-id="098be-123">System.String</span></span>

## <span data-ttu-id="098be-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="098be-124">OUTPUTS</span></span>

### <span data-ttu-id="098be-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="098be-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="098be-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="098be-126">NOTES</span></span>

## <span data-ttu-id="098be-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="098be-127">RELATED LINKS</span></span>

[<span data-ttu-id="098be-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="098be-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="098be-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="098be-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="098be-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="098be-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="098be-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="098be-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="098be-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="098be-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="098be-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="098be-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
