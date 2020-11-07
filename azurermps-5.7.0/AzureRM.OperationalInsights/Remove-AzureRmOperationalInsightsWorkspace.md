---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: d35797c007702f66bd462281a2531055524aeff5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679273"
---
# <span data-ttu-id="bf263-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf263-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="bf263-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf263-102">SYNOPSIS</span></span>
<span data-ttu-id="bf263-103">Munkaterület eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="bf263-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf263-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf263-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf263-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf263-105">DESCRIPTION</span></span>
<span data-ttu-id="bf263-106">A **Remove-AzureRmOperationalInsightsWorkspace** parancsmag töröl egy meglévő munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="bf263-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="bf263-107">Ha a munkaterületet egy meglévő fiókhoz kapcsolta a *Vevőkód* paraméterrel a létrehozási időponton keresztül, az eredeti fiók nem törlődik az üzemeltetési statisztika portálon.</span><span class="sxs-lookup"><span data-stu-id="bf263-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="bf263-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bf263-108">EXAMPLES</span></span>

### <span data-ttu-id="bf263-109">1. példa: munkaterület eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="bf263-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="bf263-110">Ez a parancs eltávolítja a MyWorkspace nevű munkaterületet az ContosoResourceGroup nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="bf263-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="bf263-111">2. példa: munkaterület eltávolítása a csővezeték használatával és megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="bf263-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="bf263-112">Ez a parancs a Get-AzureRmOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd átadja azt a **Remove-AzureRmOperationalInsightsWorkspace** parancsmagnak a pipeline operátorral az eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="bf263-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="bf263-113">Az *erő* paraméter megadása óta a parancs nem kéri, mielőtt eltávolítja a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="bf263-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="bf263-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf263-114">PARAMETERS</span></span>

### <span data-ttu-id="bf263-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf263-115">-DefaultProfile</span></span>
<span data-ttu-id="bf263-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bf263-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf263-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bf263-117">-Force</span></span>
<span data-ttu-id="bf263-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="bf263-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf263-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf263-119">-Name</span></span>
<span data-ttu-id="bf263-120">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf263-120">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf263-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf263-121">-ResourceGroupName</span></span>
<span data-ttu-id="bf263-122">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf263-122">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf263-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf263-123">-Confirm</span></span>
<span data-ttu-id="bf263-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf263-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf263-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf263-125">-WhatIf</span></span>
<span data-ttu-id="bf263-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf263-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf263-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf263-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf263-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf263-128">CommonParameters</span></span>
<span data-ttu-id="bf263-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf263-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf263-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf263-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf263-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf263-131">INPUTS</span></span>

### <span data-ttu-id="bf263-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="bf263-132">None</span></span>
<span data-ttu-id="bf263-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bf263-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf263-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf263-134">OUTPUTS</span></span>

## <span data-ttu-id="bf263-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf263-135">NOTES</span></span>

## <span data-ttu-id="bf263-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf263-136">RELATED LINKS</span></span>

[<span data-ttu-id="bf263-137">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf263-137">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="bf263-138">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf263-138">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


