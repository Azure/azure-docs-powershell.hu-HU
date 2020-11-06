---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491919"
---
# <span data-ttu-id="ccedd-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="ccedd-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="ccedd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccedd-102">SYNOPSIS</span></span>
<span data-ttu-id="ccedd-103">Tartalom eltávolítása a bejárati ajtón</span><span class="sxs-lookup"><span data-stu-id="ccedd-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccedd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccedd-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccedd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccedd-105">DESCRIPTION</span></span>
<span data-ttu-id="ccedd-106">A gyorsítótárazott tartalom Remove-AzureRmFrontDoorContent kiürítése a bejárati ajtón</span><span class="sxs-lookup"><span data-stu-id="ccedd-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="ccedd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ccedd-107">EXAMPLES</span></span>

### <span data-ttu-id="ccedd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ccedd-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="ccedd-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccedd-109">PARAMETERS</span></span>

### <span data-ttu-id="ccedd-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="ccedd-110">-ContentPath</span></span>
<span data-ttu-id="ccedd-111">A kitisztítani kívánt tartalom elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ccedd-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccedd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccedd-112">-DefaultProfile</span></span>
<span data-ttu-id="ccedd-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccedd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccedd-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ccedd-114">-Name</span></span>
<span data-ttu-id="ccedd-115">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="ccedd-115">Front Door name.</span></span>

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

### <span data-ttu-id="ccedd-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccedd-116">-PassThru</span></span>
<span data-ttu-id="ccedd-117">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="ccedd-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="ccedd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccedd-118">-ResourceGroupName</span></span>
<span data-ttu-id="ccedd-119">A bejárati ajtó csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="ccedd-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="ccedd-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccedd-120">-Confirm</span></span>
<span data-ttu-id="ccedd-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccedd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccedd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccedd-122">-WhatIf</span></span>
<span data-ttu-id="ccedd-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ccedd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccedd-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccedd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccedd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccedd-125">CommonParameters</span></span>
<span data-ttu-id="ccedd-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccedd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccedd-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccedd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccedd-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccedd-128">INPUTS</span></span>

### <span data-ttu-id="ccedd-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="ccedd-129">None</span></span>

## <span data-ttu-id="ccedd-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccedd-130">OUTPUTS</span></span>

### <span data-ttu-id="ccedd-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ccedd-131">System.Boolean</span></span>

## <span data-ttu-id="ccedd-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccedd-132">NOTES</span></span>

## <span data-ttu-id="ccedd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccedd-133">RELATED LINKS</span></span>
