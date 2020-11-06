---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 796000ac20ab887d4abd26039da2a111a19141ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497827"
---
# <span data-ttu-id="1619b-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1619b-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="1619b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1619b-102">SYNOPSIS</span></span>
<span data-ttu-id="1619b-103">Az Azure-ról származó elérhetőségi készlet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1619b-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1619b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1619b-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1619b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1619b-105">DESCRIPTION</span></span>
<span data-ttu-id="1619b-106">A **Remove-AzureRmAvailabilitySet** parancsmag az Azure-ról származó elérhetőségi készletet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="1619b-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="1619b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1619b-107">EXAMPLES</span></span>

### <span data-ttu-id="1619b-108">Példa 1: elérhetőségi készlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1619b-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1619b-109">Ez a parancs eltávolítja a ResourceGroup11 nevű erőforráscsoport AvailablitySet03 nevű elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="1619b-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1619b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1619b-110">PARAMETERS</span></span>

### <span data-ttu-id="1619b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1619b-111">-DefaultProfile</span></span>
<span data-ttu-id="1619b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1619b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1619b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1619b-113">-Force</span></span>
<span data-ttu-id="1619b-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1619b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1619b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1619b-115">-Name</span></span>
<span data-ttu-id="1619b-116">Az elérhetőség beállítása név.</span><span class="sxs-lookup"><span data-stu-id="1619b-116">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1619b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1619b-117">-ResourceGroupName</span></span>
<span data-ttu-id="1619b-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1619b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1619b-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1619b-119">-Confirm</span></span>
<span data-ttu-id="1619b-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1619b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1619b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1619b-121">-WhatIf</span></span>
<span data-ttu-id="1619b-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1619b-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1619b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1619b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1619b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1619b-124">CommonParameters</span></span>
<span data-ttu-id="1619b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1619b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1619b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1619b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1619b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1619b-127">INPUTS</span></span>

## <span data-ttu-id="1619b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1619b-128">OUTPUTS</span></span>

## <span data-ttu-id="1619b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1619b-129">NOTES</span></span>

## <span data-ttu-id="1619b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1619b-130">RELATED LINKS</span></span>

[<span data-ttu-id="1619b-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1619b-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="1619b-132">Új – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1619b-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


