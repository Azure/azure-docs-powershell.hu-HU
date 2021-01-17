---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479105"
---
# <span data-ttu-id="27de1-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="27de1-101">Update-AzAlertState</span></span>

## <span data-ttu-id="27de1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27de1-102">SYNOPSIS</span></span>
<span data-ttu-id="27de1-103">Frissítések riasztási állapota</span><span class="sxs-lookup"><span data-stu-id="27de1-103">Updates alert state</span></span>

## <span data-ttu-id="27de1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27de1-104">SYNTAX</span></span>

### <span data-ttu-id="27de1-105">ByAlertId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27de1-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27de1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27de1-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27de1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27de1-107">DESCRIPTION</span></span>
<span data-ttu-id="27de1-108">**Update-AzAlertState** parancsmag frissítési riasztási állapota.</span><span class="sxs-lookup"><span data-stu-id="27de1-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="27de1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27de1-109">EXAMPLES</span></span>

### <span data-ttu-id="27de1-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="27de1-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="27de1-111">Ez a parancsmag lezárt állapotra frissíti a riasztási állapotot.</span><span class="sxs-lookup"><span data-stu-id="27de1-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="27de1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27de1-112">PARAMETERS</span></span>

### <span data-ttu-id="27de1-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="27de1-113">-AlertId</span></span>
<span data-ttu-id="27de1-114">Riasztás/Erőforrásazonosító egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27de1-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="27de1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27de1-115">-DefaultProfile</span></span>
<span data-ttu-id="27de1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27de1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27de1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27de1-117">-InputObject</span></span>
<span data-ttu-id="27de1-118">Input object from pipeline.</span><span class="sxs-lookup"><span data-stu-id="27de1-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="27de1-119">-State</span><span class="sxs-lookup"><span data-stu-id="27de1-119">-State</span></span>
<span data-ttu-id="27de1-120">Frissített értesítési állapot</span><span class="sxs-lookup"><span data-stu-id="27de1-120">Updated Alert State</span></span>

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

### <span data-ttu-id="27de1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27de1-121">-Confirm</span></span>
<span data-ttu-id="27de1-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="27de1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27de1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27de1-123">-WhatIf</span></span>
<span data-ttu-id="27de1-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="27de1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27de1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27de1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27de1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27de1-126">CommonParameters</span></span>
<span data-ttu-id="27de1-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27de1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27de1-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27de1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27de1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27de1-129">INPUTS</span></span>

### <span data-ttu-id="27de1-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="27de1-130">None</span></span>

## <span data-ttu-id="27de1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27de1-131">OUTPUTS</span></span>

### <span data-ttu-id="27de1-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="27de1-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="27de1-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27de1-133">NOTES</span></span>

## <span data-ttu-id="27de1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27de1-134">RELATED LINKS</span></span>
