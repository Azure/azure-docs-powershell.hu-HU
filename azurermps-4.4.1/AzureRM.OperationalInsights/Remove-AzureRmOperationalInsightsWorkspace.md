---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 3f7ed1a36cc95296ee7fdeec45c5039063032d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493395"
---
# <span data-ttu-id="ba7b4-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ba7b4-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="ba7b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba7b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7b4-103">Munkaterület eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba7b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba7b4-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba7b4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba7b4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba7b4-106">A **Remove-AzureRmOperationalInsightsWorkspace** parancsmag töröl egy meglévő munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="ba7b4-107">Ha a munkaterületet egy meglévő fiókhoz kapcsolta a *Vevőkód* paraméterrel a létrehozási időponton keresztül, az eredeti fiók nem törlődik az üzemeltetési statisztika portálon.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="ba7b4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ba7b4-108">EXAMPLES</span></span>

### <span data-ttu-id="ba7b4-109">1. példa: munkaterület eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="ba7b4-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="ba7b4-110">Ez a parancs eltávolítja a MyWorkspace nevű munkaterületet az ContosoResourceGroup nevű erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ba7b4-111">2. példa: munkaterület eltávolítása a csővezeték használatával és megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="ba7b4-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="ba7b4-112">Ez a parancs a Get-AzureRmOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd átadja azt a **Remove-AzureRmOperationalInsightsWorkspace** parancsmagnak a pipeline operátorral az eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="ba7b4-113">Az *erő* paraméter megadása óta a parancs nem kéri, mielőtt eltávolítja a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="ba7b4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba7b4-114">PARAMETERS</span></span>

### <span data-ttu-id="ba7b4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ba7b4-115">-Force</span></span>
<span data-ttu-id="ba7b4-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba7b4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba7b4-117">-Name</span></span>
<span data-ttu-id="ba7b4-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-118">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="ba7b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba7b4-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="ba7b4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba7b4-121">-Confirm</span></span>
<span data-ttu-id="ba7b4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba7b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba7b4-123">-WhatIf</span></span>
<span data-ttu-id="ba7b4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba7b4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba7b4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7b4-126">-DefaultProfile</span></span>
<span data-ttu-id="ba7b4-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba7b4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7b4-128">CommonParameters</span></span>
<span data-ttu-id="ba7b4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba7b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7b4-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba7b4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7b4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba7b4-131">INPUTS</span></span>

## <span data-ttu-id="ba7b4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba7b4-132">OUTPUTS</span></span>

## <span data-ttu-id="ba7b4-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba7b4-133">NOTES</span></span>

## <span data-ttu-id="ba7b4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba7b4-134">RELATED LINKS</span></span>

[<span data-ttu-id="ba7b4-135">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ba7b4-135">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="ba7b4-136">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ba7b4-136">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


