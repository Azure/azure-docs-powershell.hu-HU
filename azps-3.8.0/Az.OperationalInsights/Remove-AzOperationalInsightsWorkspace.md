---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: ac3cda3e6c83106ac299dbd57cba81001f644305
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017286"
---
# <span data-ttu-id="b8d29-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b8d29-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="b8d29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8d29-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d29-103">Munkaterület eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b8d29-103">Removes a workspace.</span></span>

## <span data-ttu-id="b8d29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8d29-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8d29-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8d29-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d29-106">A **Remove-AzOperationalInsightsWorkspace** parancsmag töröl egy meglévő munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="b8d29-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="b8d29-107">Ha a munkaterületet egy meglévő fiókhoz kapcsolta a *Vevőkód* paraméterrel a létrehozási időponton keresztül, az eredeti fiók nem törlődik az üzemeltetési statisztika portálon.</span><span class="sxs-lookup"><span data-stu-id="b8d29-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="b8d29-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b8d29-108">EXAMPLES</span></span>

### <span data-ttu-id="b8d29-109">1. példa: munkaterület eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="b8d29-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="b8d29-110">Ez a parancs eltávolítja a MyWorkspace nevű munkaterületet az ContosoResourceGroup nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="b8d29-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="b8d29-111">2. példa: munkaterület eltávolítása a csővezeték használatával és megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="b8d29-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="b8d29-112">Ez a parancs a Get-AzOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd átadja azt a **Remove-AzOperationalInsightsWorkspace** parancsmagnak a pipeline operátorral az eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="b8d29-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="b8d29-113">Az *erő* paraméter megadása óta a parancs nem kéri, mielőtt eltávolítja a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="b8d29-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="b8d29-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8d29-114">PARAMETERS</span></span>

### <span data-ttu-id="b8d29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d29-115">-DefaultProfile</span></span>
<span data-ttu-id="b8d29-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8d29-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8d29-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b8d29-117">-Force</span></span>
<span data-ttu-id="b8d29-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b8d29-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8d29-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8d29-119">-Name</span></span>
<span data-ttu-id="b8d29-120">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8d29-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="b8d29-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d29-121">-ResourceGroupName</span></span>
<span data-ttu-id="b8d29-122">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8d29-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="b8d29-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8d29-123">-Confirm</span></span>
<span data-ttu-id="b8d29-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8d29-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d29-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d29-125">-WhatIf</span></span>
<span data-ttu-id="b8d29-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8d29-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d29-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8d29-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d29-128">CommonParameters</span></span>
<span data-ttu-id="b8d29-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8d29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d29-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d29-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d29-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8d29-131">INPUTS</span></span>

### <span data-ttu-id="b8d29-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b8d29-132">System.String</span></span>

## <span data-ttu-id="b8d29-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8d29-133">OUTPUTS</span></span>

### <span data-ttu-id="b8d29-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="b8d29-134">System.Void</span></span>

## <span data-ttu-id="b8d29-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8d29-135">NOTES</span></span>

## <span data-ttu-id="b8d29-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8d29-136">RELATED LINKS</span></span>

[<span data-ttu-id="b8d29-137">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b8d29-137">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="b8d29-138">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b8d29-138">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


