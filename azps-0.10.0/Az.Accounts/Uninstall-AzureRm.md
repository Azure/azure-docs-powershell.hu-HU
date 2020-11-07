---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: da9fa6503e76d9af8efbdff84ebbcdd501d8232d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840993"
---
# <span data-ttu-id="9b49c-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="9b49c-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="9b49c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b49c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b49c-103">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="9b49c-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="9b49c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b49c-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b49c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b49c-105">DESCRIPTION</span></span>
<span data-ttu-id="9b49c-106">Eltávolítja az összes AzureRm-modult egy gépről.</span><span class="sxs-lookup"><span data-stu-id="9b49c-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="9b49c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9b49c-107">EXAMPLES</span></span>

### <span data-ttu-id="9b49c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9b49c-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="9b49c-109">Ha futtatja ezt a parancsot, akkor az összes AzureRm-modult eltávolítja a számítógépről annak a PowerShell-verziónak a verziójára, amelyben a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b49c-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="9b49c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b49c-110">PARAMETERS</span></span>

### <span data-ttu-id="9b49c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b49c-111">-DefaultProfile</span></span>
<span data-ttu-id="9b49c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b49c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b49c-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b49c-113">-PassThru</span></span>
<span data-ttu-id="9b49c-114">Az eltávolított modulok visszatérési listája, ha meg van adva.</span><span class="sxs-lookup"><span data-stu-id="9b49c-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="9b49c-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9b49c-115">-Confirm</span></span>
<span data-ttu-id="9b49c-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9b49c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b49c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b49c-117">-WhatIf</span></span>
<span data-ttu-id="9b49c-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b49c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b49c-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b49c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b49c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b49c-120">CommonParameters</span></span>
<span data-ttu-id="9b49c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b49c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b49c-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9b49c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b49c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b49c-123">INPUTS</span></span>

### <span data-ttu-id="9b49c-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="9b49c-124">None</span></span>

## <span data-ttu-id="9b49c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b49c-125">OUTPUTS</span></span>

### <span data-ttu-id="9b49c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9b49c-126">System.String</span></span>

## <span data-ttu-id="9b49c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b49c-127">NOTES</span></span>

## <span data-ttu-id="9b49c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b49c-128">RELATED LINKS</span></span>
