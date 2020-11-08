---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194846"
---
# <span data-ttu-id="70fe5-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="70fe5-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="70fe5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="70fe5-103">Az intelligens csoport állapotának frissítése</span><span class="sxs-lookup"><span data-stu-id="70fe5-103">Updates smart group state</span></span>

## <span data-ttu-id="70fe5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70fe5-104">SYNTAX</span></span>

### <span data-ttu-id="70fe5-105">BySmartGroupId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70fe5-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70fe5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="70fe5-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70fe5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="70fe5-107">DESCRIPTION</span></span>
<span data-ttu-id="70fe5-108">**Update-AzSmartGroupState** parancsmag frissíti az intelligens csoport állapotát.</span><span class="sxs-lookup"><span data-stu-id="70fe5-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="70fe5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="70fe5-109">EXAMPLES</span></span>

### <span data-ttu-id="70fe5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="70fe5-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="70fe5-111">Ez a parancsmag frissíti az intelligens csoport állapotát a Acknowleged.</span><span class="sxs-lookup"><span data-stu-id="70fe5-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="70fe5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70fe5-112">PARAMETERS</span></span>

### <span data-ttu-id="70fe5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fe5-113">-DefaultProfile</span></span>
<span data-ttu-id="70fe5-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70fe5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70fe5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70fe5-115">-InputObject</span></span>
<span data-ttu-id="70fe5-116">Bemeneti objektum a pipeline-ról</span><span class="sxs-lookup"><span data-stu-id="70fe5-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="70fe5-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="70fe5-117">-SmartGroupId</span></span>
<span data-ttu-id="70fe5-118">Az intelligens csoport-és ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="70fe5-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="70fe5-119">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="70fe5-119">-State</span></span>
<span data-ttu-id="70fe5-120">Frissített intelligens csoport állapota</span><span class="sxs-lookup"><span data-stu-id="70fe5-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="70fe5-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70fe5-121">-Confirm</span></span>
<span data-ttu-id="70fe5-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70fe5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70fe5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70fe5-123">-WhatIf</span></span>
<span data-ttu-id="70fe5-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70fe5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70fe5-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70fe5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70fe5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fe5-126">CommonParameters</span></span>
<span data-ttu-id="70fe5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70fe5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fe5-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70fe5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fe5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70fe5-129">INPUTS</span></span>

### <span data-ttu-id="70fe5-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="70fe5-130">None</span></span>

## <span data-ttu-id="70fe5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70fe5-131">OUTPUTS</span></span>

### <span data-ttu-id="70fe5-132">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="70fe5-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="70fe5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70fe5-133">NOTES</span></span>

## <span data-ttu-id="70fe5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70fe5-134">RELATED LINKS</span></span>
