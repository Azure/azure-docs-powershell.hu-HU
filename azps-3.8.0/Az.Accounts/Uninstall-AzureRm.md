---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011987"
---
# <span data-ttu-id="7a22f-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="7a22f-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="7a22f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a22f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a22f-103">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="7a22f-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="7a22f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a22f-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a22f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a22f-105">DESCRIPTION</span></span>
<span data-ttu-id="7a22f-106">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="7a22f-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="7a22f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a22f-107">EXAMPLES</span></span>

### <span data-ttu-id="7a22f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7a22f-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="7a22f-109">Ha futtatja ezt a parancsot, akkor az összes AzureRm-modult eltávolítja a számítógépről annak a PowerShell-verziónak a verziójára, amelyben a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a22f-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="7a22f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a22f-110">PARAMETERS</span></span>

### <span data-ttu-id="7a22f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a22f-111">-DefaultProfile</span></span>
<span data-ttu-id="7a22f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a22f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a22f-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a22f-113">-PassThru</span></span>
<span data-ttu-id="7a22f-114">Az eltávolított modulok visszatérési listája, ha meg van adva.</span><span class="sxs-lookup"><span data-stu-id="7a22f-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="7a22f-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a22f-115">-Confirm</span></span>
<span data-ttu-id="7a22f-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a22f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a22f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a22f-117">-WhatIf</span></span>
<span data-ttu-id="7a22f-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a22f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a22f-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a22f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a22f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a22f-120">CommonParameters</span></span>
<span data-ttu-id="7a22f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a22f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a22f-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a22f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a22f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a22f-123">INPUTS</span></span>

### <span data-ttu-id="7a22f-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="7a22f-124">None</span></span>

## <span data-ttu-id="7a22f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a22f-125">OUTPUTS</span></span>

### <span data-ttu-id="7a22f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7a22f-126">System.String</span></span>

## <span data-ttu-id="7a22f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a22f-127">NOTES</span></span>

## <span data-ttu-id="7a22f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a22f-128">RELATED LINKS</span></span>
