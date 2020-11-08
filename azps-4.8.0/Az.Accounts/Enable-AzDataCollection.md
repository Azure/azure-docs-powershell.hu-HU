---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181924"
---
# <span data-ttu-id="cc41a-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="cc41a-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="cc41a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc41a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc41a-103">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az Azure PowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="cc41a-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="cc41a-104">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="cc41a-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="cc41a-105">Az adatokat alapértelmezés szerint gyűjtjük, hacsak nem kifejezetten kikapcsolja.</span><span class="sxs-lookup"><span data-stu-id="cc41a-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="cc41a-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc41a-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc41a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc41a-107">DESCRIPTION</span></span>

<span data-ttu-id="cc41a-108">A `Enable-AzDataCollection` parancsmag az adatgyűjtéshez való csatlakozáshoz használható.</span><span class="sxs-lookup"><span data-stu-id="cc41a-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="cc41a-109">Az Azure PowerShell alapértelmezés szerint automatikusan gyűjti a telemetriai adatokat.</span><span class="sxs-lookup"><span data-stu-id="cc41a-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="cc41a-110">A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére, valamint az Azure PowerShell használatának javítására.</span><span class="sxs-lookup"><span data-stu-id="cc41a-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="cc41a-111">A Microsoft Azure PowerShell nem gyűjt semmilyen személyes vagy személyes adatot.</span><span class="sxs-lookup"><span data-stu-id="cc41a-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="cc41a-112">Ha le szeretné tiltani az adatgyűjtést, a végrehajtáshoz explicit módon kell kiválasztania `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="cc41a-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="cc41a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="cc41a-113">EXAMPLES</span></span>

### <span data-ttu-id="cc41a-114">1. példa: adatgyűjtés engedélyezése az aktuális felhasználónál</span><span class="sxs-lookup"><span data-stu-id="cc41a-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="cc41a-115">Az alábbi példa azt szemlélteti, hogy miként engedélyezheti az aktuális felhasználó adatgyűjtését.</span><span class="sxs-lookup"><span data-stu-id="cc41a-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="cc41a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc41a-116">PARAMETERS</span></span>

### <span data-ttu-id="cc41a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc41a-117">-DefaultProfile</span></span>

<span data-ttu-id="cc41a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc41a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc41a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc41a-119">-Confirm</span></span>

<span data-ttu-id="cc41a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc41a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc41a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc41a-121">-WhatIf</span></span>

<span data-ttu-id="cc41a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc41a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc41a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc41a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc41a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc41a-124">CommonParameters</span></span>

<span data-ttu-id="cc41a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc41a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc41a-126">További információt a [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc41a-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="cc41a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc41a-127">INPUTS</span></span>

### <span data-ttu-id="cc41a-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="cc41a-128">None</span></span>

## <span data-ttu-id="cc41a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc41a-129">OUTPUTS</span></span>

### <span data-ttu-id="cc41a-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="cc41a-130">System.Void</span></span>

## <span data-ttu-id="cc41a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc41a-131">NOTES</span></span>

## <span data-ttu-id="cc41a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc41a-132">RELATED LINKS</span></span>

[<span data-ttu-id="cc41a-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="cc41a-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
