---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194845"
---
# <span data-ttu-id="e7df4-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="e7df4-101">Update-AzAlertState</span></span>

## <span data-ttu-id="e7df4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7df4-102">SYNOPSIS</span></span>
<span data-ttu-id="e7df4-103">Riasztási állapot frissítése</span><span class="sxs-lookup"><span data-stu-id="e7df4-103">Updates alert state</span></span>

## <span data-ttu-id="e7df4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7df4-104">SYNTAX</span></span>

### <span data-ttu-id="e7df4-105">ByAlertId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7df4-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7df4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e7df4-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7df4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7df4-107">DESCRIPTION</span></span>
<span data-ttu-id="e7df4-108">**Update-AzAlertState** parancsmag: a frissítések riasztási állapota.</span><span class="sxs-lookup"><span data-stu-id="e7df4-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="e7df4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e7df4-109">EXAMPLES</span></span>

### <span data-ttu-id="e7df4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7df4-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="e7df4-111">Ez a parancsmag a riasztási állapotot a bezárásra frissíti.</span><span class="sxs-lookup"><span data-stu-id="e7df4-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="e7df4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7df4-112">PARAMETERS</span></span>

### <span data-ttu-id="e7df4-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="e7df4-113">-AlertId</span></span>
<span data-ttu-id="e7df4-114">Értesítési/ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e7df4-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7df4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7df4-115">-DefaultProfile</span></span>
<span data-ttu-id="e7df4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7df4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7df4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7df4-117">-InputObject</span></span>
<span data-ttu-id="e7df4-118">Bemeneti objektum a pipeline-ról</span><span class="sxs-lookup"><span data-stu-id="e7df4-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7df4-119">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="e7df4-119">-State</span></span>
<span data-ttu-id="e7df4-120">Frissített riasztási állapot</span><span class="sxs-lookup"><span data-stu-id="e7df4-120">Updated Alert State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7df4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7df4-121">-Confirm</span></span>
<span data-ttu-id="e7df4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7df4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7df4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7df4-123">-WhatIf</span></span>
<span data-ttu-id="e7df4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7df4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7df4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7df4-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7df4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7df4-126">CommonParameters</span></span>
<span data-ttu-id="e7df4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7df4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7df4-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e7df4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7df4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7df4-129">INPUTS</span></span>

### <span data-ttu-id="e7df4-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7df4-130">None</span></span>

## <span data-ttu-id="e7df4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7df4-131">OUTPUTS</span></span>

### <span data-ttu-id="e7df4-132">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="e7df4-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="e7df4-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7df4-133">NOTES</span></span>

## <span data-ttu-id="e7df4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7df4-134">RELATED LINKS</span></span>