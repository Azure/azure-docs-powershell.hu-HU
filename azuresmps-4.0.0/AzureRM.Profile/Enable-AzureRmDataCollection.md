---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491176"
---
# <span data-ttu-id="33fc3-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="33fc3-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="33fc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="33fc3-103">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="33fc3-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="33fc3-104">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="33fc3-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="33fc3-105">Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.</span><span class="sxs-lookup"><span data-stu-id="33fc3-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="33fc3-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33fc3-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33fc3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="33fc3-107">DESCRIPTION</span></span>
<span data-ttu-id="33fc3-108">Javíthatja a Microsoft Cloud és az Azure PowerShell használatával kapcsolatos tapasztalatokat az adatgyűjtés kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="33fc3-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="33fc3-109">Az Azure PowerShell nem gyűjti össze az adatokat a hozzájárulása nélkül – az engedélyezés – AzureRmDataCollection, vagy ha az Azure PowerShell kéri az adatok gyűjtését a parancsmag első futtatásakor.</span><span class="sxs-lookup"><span data-stu-id="33fc3-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="33fc3-110">A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére és az Azure PowerShell használatba vétele érdekében.</span><span class="sxs-lookup"><span data-stu-id="33fc3-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="33fc3-111">A Microsoft Azure PowerShell semmilyen személyes adatot nem gyűjt, vagy bármilyen személyazonosításra alkalmas információt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="33fc3-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="33fc3-112">Futtassa az Enable-AzureRMDataCollection parancsmagot az aktuális számítógépen az aktuális felhasználó adatgyűjtése engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="33fc3-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="33fc3-113">Ez megakadályozza, hogy az aktuális felhasználó Kérdezzen az adatgyűjtésről az első időparancsmagok végrehajtása során.</span><span class="sxs-lookup"><span data-stu-id="33fc3-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="33fc3-114">Az aktuális felhasználó adatgyűjtésének letiltásához futtassa az Disable-AzureRmDataCollection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="33fc3-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="33fc3-115">Példák</span><span class="sxs-lookup"><span data-stu-id="33fc3-115">EXAMPLES</span></span>

### <span data-ttu-id="33fc3-116">1. példa: adatgyűjtés engedélyezése az aktuális felhasználónál</span><span class="sxs-lookup"><span data-stu-id="33fc3-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="33fc3-117">Ebben a példában bemutatjuk, hogy miként engedélyezheti az aktuális felhasználó adatgyűjtését.</span><span class="sxs-lookup"><span data-stu-id="33fc3-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="33fc3-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33fc3-118">PARAMETERS</span></span>

### <span data-ttu-id="33fc3-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="33fc3-119">-Confirm</span></span>
<span data-ttu-id="33fc3-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="33fc3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33fc3-121">-WhatIf</span></span>
<span data-ttu-id="33fc3-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="33fc3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33fc3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33fc3-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fc3-124">CommonParameters</span></span>
<span data-ttu-id="33fc3-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33fc3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fc3-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33fc3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fc3-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33fc3-127">INPUTS</span></span>

## <span data-ttu-id="33fc3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33fc3-128">OUTPUTS</span></span>

### <span data-ttu-id="33fc3-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="33fc3-129">None</span></span>

## <span data-ttu-id="33fc3-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33fc3-130">NOTES</span></span>

## <span data-ttu-id="33fc3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33fc3-131">RELATED LINKS</span></span>

[<span data-ttu-id="33fc3-132">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="33fc3-132">Disable-AzureRmDataCollection</span></span>]()

