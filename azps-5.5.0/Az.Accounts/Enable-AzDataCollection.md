---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162667"
---
# <span data-ttu-id="d0f45-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d0f45-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="d0f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f45-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f45-103">Lehetővé teszi, hogy az Azure PowerShell adatokat gyűjtsön az Azure PowerShell-parancsmagok felhasználói élményének javításához.</span><span class="sxs-lookup"><span data-stu-id="d0f45-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="d0f45-104">A parancsmag végrehajtása az aktuális gép aktuális felhasználója számára is be van jelentkezve az adatgyűjtésbe.</span><span class="sxs-lookup"><span data-stu-id="d0f45-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="d0f45-105">Az adatokat alapértelmezés szerint gyűjtjük, hacsak Ön kifejezetten nem tiltja le.</span><span class="sxs-lookup"><span data-stu-id="d0f45-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="d0f45-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0f45-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f45-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0f45-107">DESCRIPTION</span></span>

<span data-ttu-id="d0f45-108">A `Enable-AzDataCollection` parancsmag az adatgyűjtésre való feliratkozásra használható.</span><span class="sxs-lookup"><span data-stu-id="d0f45-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="d0f45-109">Az Azure PowerShell alapértelmezés szerint automatikusan telemetriai adatokat gyűjt.</span><span class="sxs-lookup"><span data-stu-id="d0f45-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="d0f45-110">A Microsoft összegyűjti az összegyűjtött adatokat a használati minták azonosítása, a gyakori problémák azonosítása és az Azure PowerShell használatának javítása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d0f45-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="d0f45-111">A Microsoft Azure PowerShell nem gyűjt személyes vagy személyes adatokat.</span><span class="sxs-lookup"><span data-stu-id="d0f45-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="d0f45-112">Az adatgyűjtés letiltásához a végrehajtást kifejezetten le kell `Disable-AzDataCollection` tiltania.</span><span class="sxs-lookup"><span data-stu-id="d0f45-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="d0f45-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0f45-113">EXAMPLES</span></span>

### <span data-ttu-id="d0f45-114">1. példa: Adatgyűjtés engedélyezése az aktuális felhasználó számára</span><span class="sxs-lookup"><span data-stu-id="d0f45-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="d0f45-115">Az alábbi példa bemutatja, hogyan engedélyezheti az adatgyűjtést az aktuális felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="d0f45-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="d0f45-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0f45-116">PARAMETERS</span></span>

### <span data-ttu-id="d0f45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f45-117">-DefaultProfile</span></span>

<span data-ttu-id="d0f45-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0f45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f45-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0f45-119">-Confirm</span></span>

<span data-ttu-id="d0f45-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0f45-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f45-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f45-121">-WhatIf</span></span>

<span data-ttu-id="d0f45-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0f45-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0f45-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0f45-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f45-124">CommonParameters</span></span>

<span data-ttu-id="d0f45-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f45-126">További információt a [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="d0f45-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="d0f45-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0f45-127">INPUTS</span></span>

### <span data-ttu-id="d0f45-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d0f45-128">None</span></span>

## <span data-ttu-id="d0f45-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0f45-129">OUTPUTS</span></span>

### <span data-ttu-id="d0f45-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d0f45-130">System.Void</span></span>

## <span data-ttu-id="d0f45-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0f45-131">NOTES</span></span>

## <span data-ttu-id="d0f45-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0f45-132">RELATED LINKS</span></span>

[<span data-ttu-id="d0f45-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d0f45-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
