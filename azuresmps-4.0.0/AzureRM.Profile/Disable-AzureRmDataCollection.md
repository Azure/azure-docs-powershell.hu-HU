---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e233c523e5fd9372b1e7dd86b5b5e73eb3f7091e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491180"
---
# <span data-ttu-id="a52ac-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="a52ac-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="a52ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a52ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a52ac-103">A AzurePowerShell-parancsmagok fejlesztéséhez kimarad az adatok gyűjtése.</span><span class="sxs-lookup"><span data-stu-id="a52ac-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="a52ac-104">Az adatokat csak akkor gyűjti össze, ha kifejezetten bejelöli.</span><span class="sxs-lookup"><span data-stu-id="a52ac-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="a52ac-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a52ac-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a52ac-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="a52ac-106">DESCRIPTION</span></span>
<span data-ttu-id="a52ac-107">Javíthatja a Microsoft Cloud és az Azure PowerShell használatával kapcsolatos tapasztalatokat az adatgyűjtés kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="a52ac-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="a52ac-108">Az Azure PowerShell nem gyűjti össze az adatokat a hozzájárulása nélkül – az engedélyezés – AzureRmDataCollection, vagy ha az Azure PowerShell kéri az adatok gyűjtését a parancsmag első futtatásakor.</span><span class="sxs-lookup"><span data-stu-id="a52ac-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="a52ac-109">A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére és az Azure PowerShell használatba vétele érdekében.</span><span class="sxs-lookup"><span data-stu-id="a52ac-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="a52ac-110">A Microsoft Azure PowerShell semmilyen személyes adatot nem gyűjt, vagy bármilyen személyazonosításra alkalmas információt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a52ac-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="a52ac-111">A Disable-AzureRMDataCollection parancsmag futtatásával tiltsa le az aktuális felhasználó adatgyűjtési szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="a52ac-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="a52ac-112">Ez megakadályozza, hogy az aktuális felhasználó Kérdezzen az adatgyűjtésről az első időparancsmagok végrehajtása során.</span><span class="sxs-lookup"><span data-stu-id="a52ac-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="a52ac-113">Ha engedélyezni szeretné a jelenlegi felhasználó adatgyűjtését, futtassa az Enable-AzureRmDataCollection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a52ac-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="a52ac-114">Példák</span><span class="sxs-lookup"><span data-stu-id="a52ac-114">EXAMPLES</span></span>

### <span data-ttu-id="a52ac-115">1. példa: az aktuális felhasználó adatgyűjtésének letiltása</span><span class="sxs-lookup"><span data-stu-id="a52ac-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="a52ac-116">Ez a példa bemutatja, hogyan tilthatja le az aktuális felhasználó adatgyűjtését.</span><span class="sxs-lookup"><span data-stu-id="a52ac-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="a52ac-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a52ac-117">PARAMETERS</span></span>

### <span data-ttu-id="a52ac-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a52ac-118">-Confirm</span></span>
<span data-ttu-id="a52ac-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a52ac-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a52ac-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a52ac-120">-WhatIf</span></span>
<span data-ttu-id="a52ac-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a52ac-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a52ac-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a52ac-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a52ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52ac-123">CommonParameters</span></span>
<span data-ttu-id="a52ac-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a52ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52ac-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52ac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52ac-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a52ac-126">INPUTS</span></span>

## <span data-ttu-id="a52ac-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a52ac-127">OUTPUTS</span></span>

### <span data-ttu-id="a52ac-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="a52ac-128">None</span></span>

## <span data-ttu-id="a52ac-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a52ac-129">NOTES</span></span>

## <span data-ttu-id="a52ac-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a52ac-130">RELATED LINKS</span></span>

[<span data-ttu-id="a52ac-131">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="a52ac-131">Enable-AzureRmDataCollection</span></span>]()

