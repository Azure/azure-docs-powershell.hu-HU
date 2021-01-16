---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344994"
---
# <span data-ttu-id="dccca-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="dccca-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="dccca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dccca-102">SYNOPSIS</span></span>
<span data-ttu-id="dccca-103">Intelligens csoport állapotának frissítése</span><span class="sxs-lookup"><span data-stu-id="dccca-103">Updates smart group state</span></span>

## <span data-ttu-id="dccca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dccca-104">SYNTAX</span></span>

### <span data-ttu-id="dccca-105">BySmartGroupId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dccca-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dccca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dccca-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dccca-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dccca-107">DESCRIPTION</span></span>
<span data-ttu-id="dccca-108">**Update-AzSmartGroupState** parancsmag frissíti az intelligens csoport állapotát.</span><span class="sxs-lookup"><span data-stu-id="dccca-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="dccca-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dccca-109">EXAMPLES</span></span>

### <span data-ttu-id="dccca-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="dccca-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="dccca-111">Ez a parancsmag az intelligens csoport állapotát Acknowleged állapotra frissíti.</span><span class="sxs-lookup"><span data-stu-id="dccca-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="dccca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dccca-112">PARAMETERS</span></span>

### <span data-ttu-id="dccca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccca-113">-DefaultProfile</span></span>
<span data-ttu-id="dccca-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dccca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dccca-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dccca-115">-InputObject</span></span>
<span data-ttu-id="dccca-116">Input object from pipeline.</span><span class="sxs-lookup"><span data-stu-id="dccca-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dccca-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="dccca-117">-SmartGroupId</span></span>
<span data-ttu-id="dccca-118">Az intelligens csoport intelligens csoportjának/Erőforrásazonosítójának egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dccca-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccca-119">-State</span><span class="sxs-lookup"><span data-stu-id="dccca-119">-State</span></span>
<span data-ttu-id="dccca-120">Frissített intelligens csoport állapota</span><span class="sxs-lookup"><span data-stu-id="dccca-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="dccca-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dccca-121">-Confirm</span></span>
<span data-ttu-id="dccca-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dccca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dccca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dccca-123">-WhatIf</span></span>
<span data-ttu-id="dccca-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dccca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dccca-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dccca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dccca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccca-126">CommonParameters</span></span>
<span data-ttu-id="dccca-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccca-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dccca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccca-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dccca-129">INPUTS</span></span>

### <span data-ttu-id="dccca-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="dccca-130">None</span></span>

## <span data-ttu-id="dccca-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dccca-131">OUTPUTS</span></span>

### <span data-ttu-id="dccca-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="dccca-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="dccca-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dccca-133">NOTES</span></span>

## <span data-ttu-id="dccca-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dccca-134">RELATED LINKS</span></span>
