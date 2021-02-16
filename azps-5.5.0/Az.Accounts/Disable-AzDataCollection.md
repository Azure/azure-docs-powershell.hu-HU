---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162690"
---
# <span data-ttu-id="ce50e-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ce50e-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="ce50e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce50e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce50e-103">Az Azure PowerShell-parancsmagok fejlesztése érdekében nem gyűjt adatokat.</span><span class="sxs-lookup"><span data-stu-id="ce50e-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ce50e-104">Az adatokat alapértelmezés szerint gyűjtjük, hacsak Ön kifejezetten le nem tiltja.</span><span class="sxs-lookup"><span data-stu-id="ce50e-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="ce50e-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ce50e-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce50e-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ce50e-106">DESCRIPTION</span></span>

<span data-ttu-id="ce50e-107">A parancsmag az adatgyűjtés `Disable-AzDataCollection` letiltása.</span><span class="sxs-lookup"><span data-stu-id="ce50e-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="ce50e-108">Az Azure PowerShell alapértelmezés szerint automatikusan telemetriai adatokat gyűjt.</span><span class="sxs-lookup"><span data-stu-id="ce50e-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="ce50e-109">Az adatgyűjtés letiltásához explicit módon le kell tiltania az adatgyűjtést. A Microsoft összegyűjti az összegyűjtött adatokat a használati minták azonosítása, a gyakori problémák azonosítása és az Azure PowerShell használatának javítása érdekében.</span><span class="sxs-lookup"><span data-stu-id="ce50e-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="ce50e-110">A Microsoft Azure PowerShell nem gyűjt személyes vagy személyes adatokat.</span><span class="sxs-lookup"><span data-stu-id="ce50e-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="ce50e-111">Ha korábban már kikapcsolta, a parancsmag futtatásával engedélyezze újra az adatgyűjtést az aktuális gépen `Enable-AzDataCollection` lévő felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="ce50e-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="ce50e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ce50e-112">EXAMPLES</span></span>

### <span data-ttu-id="ce50e-113">1. példa: Az aktuális felhasználó adatgyűjtésének letiltása</span><span class="sxs-lookup"><span data-stu-id="ce50e-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="ce50e-114">Az alábbi példa bemutatja, hogyan tilthatja le az adatgyűjtést az aktuális felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="ce50e-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="ce50e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce50e-115">PARAMETERS</span></span>

### <span data-ttu-id="ce50e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce50e-116">-DefaultProfile</span></span>

<span data-ttu-id="ce50e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce50e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce50e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce50e-118">-Confirm</span></span>

<span data-ttu-id="ce50e-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ce50e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce50e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce50e-120">-WhatIf</span></span>

<span data-ttu-id="ce50e-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ce50e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce50e-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce50e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce50e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce50e-123">CommonParameters</span></span>

<span data-ttu-id="ce50e-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce50e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce50e-125">További információt a [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="ce50e-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="ce50e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce50e-126">INPUTS</span></span>

### <span data-ttu-id="ce50e-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="ce50e-127">None</span></span>

## <span data-ttu-id="ce50e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce50e-128">OUTPUTS</span></span>

### <span data-ttu-id="ce50e-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="ce50e-129">System.Void</span></span>

## <span data-ttu-id="ce50e-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ce50e-130">NOTES</span></span>

## <span data-ttu-id="ce50e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce50e-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce50e-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ce50e-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
