---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 93c51e71cf912a072daafd721d9e9626ccefbb06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849297"
---
# <span data-ttu-id="2c407-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2c407-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="2c407-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c407-102">SYNOPSIS</span></span>
<span data-ttu-id="2c407-103">Az automéretarány beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2c407-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c407-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c407-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c407-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c407-105">DESCRIPTION</span></span>
<span data-ttu-id="2c407-106">A **Remove-AzureRmAutoscaleSetting** parancsmag automatikusan eltávolítja az automéretarány beállítást.</span><span class="sxs-lookup"><span data-stu-id="2c407-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="2c407-107">Meg kell adnia a beállítás nevét, valamint annak az erőforrás-csoportnak a nevét, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2c407-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="2c407-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="2c407-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2c407-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2c407-109">EXAMPLES</span></span>

## <span data-ttu-id="2c407-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c407-110">PARAMETERS</span></span>

### <span data-ttu-id="2c407-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c407-111">-DefaultProfile</span></span>
<span data-ttu-id="2c407-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2c407-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c407-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c407-113">-Name</span></span>
<span data-ttu-id="2c407-114">Az eltávolítandó méretezési beállítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c407-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="2c407-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c407-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c407-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c407-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2c407-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c407-117">-Confirm</span></span>
<span data-ttu-id="2c407-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c407-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c407-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c407-119">-WhatIf</span></span>
<span data-ttu-id="2c407-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c407-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c407-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c407-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c407-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c407-122">CommonParameters</span></span>
<span data-ttu-id="2c407-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c407-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c407-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c407-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c407-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c407-125">INPUTS</span></span>

### <span data-ttu-id="2c407-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2c407-126">System.String</span></span>

## <span data-ttu-id="2c407-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c407-127">OUTPUTS</span></span>

### <span data-ttu-id="2c407-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2c407-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2c407-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c407-129">NOTES</span></span>

## <span data-ttu-id="2c407-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c407-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c407-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2c407-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="2c407-132">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2c407-132">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


