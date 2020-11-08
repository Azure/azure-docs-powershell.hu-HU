---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: 5b07928b78c8a6513e91c9e8ec21dbc27294552e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002828"
---
# <span data-ttu-id="b6b77-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b6b77-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="b6b77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6b77-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b77-103">Az automéretarány beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6b77-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="b6b77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6b77-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b77-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6b77-105">DESCRIPTION</span></span>
<span data-ttu-id="b6b77-106">A **Remove-AzAutoscaleSetting** parancsmag automatikusan eltávolítja az automéretarány beállítást.</span><span class="sxs-lookup"><span data-stu-id="b6b77-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="b6b77-107">Meg kell adnia a beállítás nevét, valamint annak az erőforrás-csoportnak a nevét, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b6b77-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="b6b77-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="b6b77-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b6b77-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b6b77-109">EXAMPLES</span></span>

## <span data-ttu-id="b6b77-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6b77-110">PARAMETERS</span></span>

### <span data-ttu-id="b6b77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b77-111">-DefaultProfile</span></span>
<span data-ttu-id="b6b77-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b6b77-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6b77-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6b77-113">-Name</span></span>
<span data-ttu-id="b6b77-114">Az eltávolítandó méretezési beállítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6b77-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="b6b77-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b77-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6b77-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6b77-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b77-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6b77-117">-Confirm</span></span>
<span data-ttu-id="b6b77-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6b77-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b77-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b77-119">-WhatIf</span></span>
<span data-ttu-id="b6b77-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6b77-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6b77-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6b77-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b77-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b77-122">CommonParameters</span></span>
<span data-ttu-id="b6b77-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6b77-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b77-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6b77-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b77-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6b77-125">INPUTS</span></span>

### <span data-ttu-id="b6b77-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b6b77-126">System.String</span></span>

## <span data-ttu-id="b6b77-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6b77-127">OUTPUTS</span></span>

### <span data-ttu-id="b6b77-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b6b77-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b6b77-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6b77-129">NOTES</span></span>

## <span data-ttu-id="b6b77-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6b77-130">RELATED LINKS</span></span>

[<span data-ttu-id="b6b77-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b6b77-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="b6b77-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b6b77-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


