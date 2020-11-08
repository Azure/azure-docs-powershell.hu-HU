---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185925"
---
# <span data-ttu-id="e32ca-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e32ca-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="e32ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e32ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e32ca-103">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e32ca-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="e32ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e32ca-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e32ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e32ca-105">DESCRIPTION</span></span>
<span data-ttu-id="e32ca-106">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e32ca-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="e32ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e32ca-107">EXAMPLES</span></span>

### <span data-ttu-id="e32ca-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e32ca-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="e32ca-109">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e32ca-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="e32ca-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e32ca-110">PARAMETERS</span></span>

### <span data-ttu-id="e32ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32ca-111">-DefaultProfile</span></span>
<span data-ttu-id="e32ca-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e32ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e32ca-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e32ca-113">-Force</span></span>
<span data-ttu-id="e32ca-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e32ca-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e32ca-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="e32ca-115">-Location</span></span>
<span data-ttu-id="e32ca-116">A munkaterület által létrehozott földrajzi terület.</span><span class="sxs-lookup"><span data-stu-id="e32ca-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32ca-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e32ca-117">-Name</span></span>
<span data-ttu-id="e32ca-118">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e32ca-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e32ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="e32ca-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e32ca-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32ca-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e32ca-121">-Confirm</span></span>
<span data-ttu-id="e32ca-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e32ca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e32ca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e32ca-123">-WhatIf</span></span>
<span data-ttu-id="e32ca-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e32ca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e32ca-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e32ca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e32ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32ca-126">CommonParameters</span></span>
<span data-ttu-id="e32ca-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e32ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32ca-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e32ca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32ca-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e32ca-129">INPUTS</span></span>

### <span data-ttu-id="e32ca-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e32ca-130">System.String</span></span>

## <span data-ttu-id="e32ca-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e32ca-131">OUTPUTS</span></span>

### <span data-ttu-id="e32ca-132">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e32ca-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e32ca-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e32ca-133">NOTES</span></span>

## <span data-ttu-id="e32ca-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e32ca-134">RELATED LINKS</span></span>
