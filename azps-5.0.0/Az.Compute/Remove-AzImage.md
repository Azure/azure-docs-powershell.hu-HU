---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186242"
---
# <span data-ttu-id="f4981-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="f4981-101">Remove-AzImage</span></span>

## <span data-ttu-id="f4981-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4981-102">SYNOPSIS</span></span>
<span data-ttu-id="f4981-103">Eltávolít egy képet.</span><span class="sxs-lookup"><span data-stu-id="f4981-103">Removes an image.</span></span>

## <span data-ttu-id="f4981-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4981-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4981-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4981-105">DESCRIPTION</span></span>
<span data-ttu-id="f4981-106">A **Remove-AzImage** parancsmag eltávolítja a képet.</span><span class="sxs-lookup"><span data-stu-id="f4981-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="f4981-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4981-107">EXAMPLES</span></span>

### <span data-ttu-id="f4981-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4981-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="f4981-109">Ez a parancs eltávolítja a "Image01" nevű képet a "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="f4981-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f4981-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4981-110">PARAMETERS</span></span>

### <span data-ttu-id="f4981-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4981-111">-AsJob</span></span>
<span data-ttu-id="f4981-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="f4981-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f4981-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4981-113">-DefaultProfile</span></span>
<span data-ttu-id="f4981-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4981-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4981-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f4981-115">-Force</span></span>
<span data-ttu-id="f4981-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f4981-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4981-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f4981-117">-ImageName</span></span>
<span data-ttu-id="f4981-118">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4981-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4981-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4981-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4981-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4981-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f4981-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4981-121">-Confirm</span></span>
<span data-ttu-id="f4981-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4981-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4981-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4981-123">-WhatIf</span></span>
<span data-ttu-id="f4981-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4981-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4981-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4981-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4981-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4981-126">CommonParameters</span></span>
<span data-ttu-id="f4981-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4981-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4981-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4981-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4981-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4981-129">INPUTS</span></span>

### <span data-ttu-id="f4981-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f4981-130">System.String</span></span>

## <span data-ttu-id="f4981-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4981-131">OUTPUTS</span></span>

### <span data-ttu-id="f4981-132">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f4981-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f4981-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4981-133">NOTES</span></span>

## <span data-ttu-id="f4981-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4981-134">RELATED LINKS</span></span>