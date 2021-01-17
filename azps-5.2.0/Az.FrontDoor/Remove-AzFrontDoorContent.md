---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332226"
---
# <span data-ttu-id="d4902-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="d4902-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="d4902-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4902-102">SYNOPSIS</span></span>
<span data-ttu-id="d4902-103">Tartalom eltávolítása a Front Doorban</span><span class="sxs-lookup"><span data-stu-id="d4902-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="d4902-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4902-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4902-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4902-105">DESCRIPTION</span></span>
<span data-ttu-id="d4902-106">Remove-AzFrontDoorContent elülső ajtó gyorsítótárazott tartalmának törlése</span><span class="sxs-lookup"><span data-stu-id="d4902-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="d4902-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4902-107">EXAMPLES</span></span>

### <span data-ttu-id="d4902-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d4902-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="d4902-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4902-109">PARAMETERS</span></span>

### <span data-ttu-id="d4902-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="d4902-110">-ContentPath</span></span>
<span data-ttu-id="d4902-111">A véglegesen meg nem ürülni.</span><span class="sxs-lookup"><span data-stu-id="d4902-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="d4902-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4902-112">-DefaultProfile</span></span>
<span data-ttu-id="d4902-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4902-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4902-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d4902-114">-Name</span></span>
<span data-ttu-id="d4902-115">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="d4902-115">Front Door name.</span></span>

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

### <span data-ttu-id="d4902-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4902-116">-PassThru</span></span>
<span data-ttu-id="d4902-117">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="d4902-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="d4902-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4902-118">-ResourceGroupName</span></span>
<span data-ttu-id="d4902-119">A Front Door erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="d4902-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="d4902-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4902-120">-Confirm</span></span>
<span data-ttu-id="d4902-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4902-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4902-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4902-122">-WhatIf</span></span>
<span data-ttu-id="d4902-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4902-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4902-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4902-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4902-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4902-125">CommonParameters</span></span>
<span data-ttu-id="d4902-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4902-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4902-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4902-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4902-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4902-128">INPUTS</span></span>

### <span data-ttu-id="d4902-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="d4902-129">None</span></span>

## <span data-ttu-id="d4902-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4902-130">OUTPUTS</span></span>

### <span data-ttu-id="d4902-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4902-131">System.Boolean</span></span>

## <span data-ttu-id="d4902-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4902-132">NOTES</span></span>

## <span data-ttu-id="d4902-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4902-133">RELATED LINKS</span></span>
