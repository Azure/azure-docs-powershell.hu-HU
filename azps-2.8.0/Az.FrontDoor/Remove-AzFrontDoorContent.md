---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: f48dedc50ae134967a57320b065389505aa9c1ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666404"
---
# <span data-ttu-id="19a0b-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="19a0b-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="19a0b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="19a0b-103">Tartalom eltávolítása a bejárati ajtón</span><span class="sxs-lookup"><span data-stu-id="19a0b-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="19a0b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19a0b-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19a0b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="19a0b-106">A gyorsítótárazott tartalom Remove-AzFrontDoorContent kiürítése a bejárati ajtón</span><span class="sxs-lookup"><span data-stu-id="19a0b-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="19a0b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19a0b-107">EXAMPLES</span></span>

### <span data-ttu-id="19a0b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19a0b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="19a0b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19a0b-109">PARAMETERS</span></span>

### <span data-ttu-id="19a0b-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="19a0b-110">-ContentPath</span></span>
<span data-ttu-id="19a0b-111">A kitisztítani kívánt tartalom elérési útja.</span><span class="sxs-lookup"><span data-stu-id="19a0b-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="19a0b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a0b-112">-DefaultProfile</span></span>
<span data-ttu-id="19a0b-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19a0b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19a0b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19a0b-114">-Name</span></span>
<span data-ttu-id="19a0b-115">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="19a0b-115">Front Door name.</span></span>

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

### <span data-ttu-id="19a0b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19a0b-116">-PassThru</span></span>
<span data-ttu-id="19a0b-117">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="19a0b-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="19a0b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19a0b-118">-ResourceGroupName</span></span>
<span data-ttu-id="19a0b-119">A bejárati ajtó csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="19a0b-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="19a0b-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19a0b-120">-Confirm</span></span>
<span data-ttu-id="19a0b-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19a0b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19a0b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19a0b-122">-WhatIf</span></span>
<span data-ttu-id="19a0b-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19a0b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19a0b-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19a0b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19a0b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a0b-125">CommonParameters</span></span>
<span data-ttu-id="19a0b-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19a0b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a0b-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="19a0b-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a0b-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19a0b-128">INPUTS</span></span>

### <span data-ttu-id="19a0b-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="19a0b-129">None</span></span>

## <span data-ttu-id="19a0b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19a0b-130">OUTPUTS</span></span>

### <span data-ttu-id="19a0b-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19a0b-131">System.Boolean</span></span>

## <span data-ttu-id="19a0b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19a0b-132">NOTES</span></span>

## <span data-ttu-id="19a0b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19a0b-133">RELATED LINKS</span></span>
