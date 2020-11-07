---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 9a6e87fb28fde1af024460a0b09d0339222d1ee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678963"
---
# <span data-ttu-id="96a1d-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="96a1d-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="96a1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="96a1d-103">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="96a1d-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="96a1d-104">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="96a1d-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="96a1d-105">Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.</span><span class="sxs-lookup"><span data-stu-id="96a1d-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96a1d-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96a1d-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96a1d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="96a1d-107">DESCRIPTION</span></span>
<span data-ttu-id="96a1d-108">Javíthatja a Microsoft Cloud és az Azure PowerShell használatával kapcsolatos tapasztalatokat az adatgyűjtés kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="96a1d-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="96a1d-109">Az Azure PowerShell nem gyűjti össze az adatokat a hozzájárulása nélkül – az engedélyezés – AzureRmDataCollection, vagy ha az Azure PowerShell kéri az adatok gyűjtését a parancsmag első futtatásakor.</span><span class="sxs-lookup"><span data-stu-id="96a1d-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="96a1d-110">A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére és az Azure PowerShell használatba vétele érdekében.</span><span class="sxs-lookup"><span data-stu-id="96a1d-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="96a1d-111">A Microsoft Azure PowerShell semmilyen személyes adatot nem gyűjt, vagy bármilyen személyazonosításra alkalmas információt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="96a1d-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="96a1d-112">Futtassa az Enable-AzureRMDataCollection parancsmagot az aktuális számítógépen az aktuális felhasználó adatgyűjtése engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="96a1d-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="96a1d-113">Ez megakadályozza, hogy az aktuális felhasználó Kérdezzen az adatgyűjtésről az első időparancsmagok végrehajtása során.</span><span class="sxs-lookup"><span data-stu-id="96a1d-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="96a1d-114">Az aktuális felhasználó adatgyűjtésének letiltásához futtassa az Disable-AzureRmDataCollection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96a1d-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="96a1d-115">Példák</span><span class="sxs-lookup"><span data-stu-id="96a1d-115">EXAMPLES</span></span>

### <span data-ttu-id="96a1d-116">1. példa: adatgyűjtés engedélyezése az aktuális felhasználónál</span><span class="sxs-lookup"><span data-stu-id="96a1d-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="96a1d-117">Ebben a példában bemutatjuk, hogy miként engedélyezheti az aktuális felhasználó adatgyűjtését.</span><span class="sxs-lookup"><span data-stu-id="96a1d-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="96a1d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96a1d-118">PARAMETERS</span></span>

### <span data-ttu-id="96a1d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a1d-119">-DefaultProfile</span></span>
<span data-ttu-id="96a1d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96a1d-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a1d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96a1d-121">-Confirm</span></span>
<span data-ttu-id="96a1d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96a1d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a1d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a1d-123">-WhatIf</span></span>
<span data-ttu-id="96a1d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96a1d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96a1d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96a1d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a1d-126">CommonParameters</span></span>
<span data-ttu-id="96a1d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96a1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a1d-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a1d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a1d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96a1d-129">INPUTS</span></span>

### <span data-ttu-id="96a1d-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="96a1d-130">None</span></span>
<span data-ttu-id="96a1d-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="96a1d-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96a1d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96a1d-132">OUTPUTS</span></span>

### <span data-ttu-id="96a1d-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="96a1d-133">None</span></span>

## <span data-ttu-id="96a1d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96a1d-134">NOTES</span></span>

## <span data-ttu-id="96a1d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96a1d-135">RELATED LINKS</span></span>

[<span data-ttu-id="96a1d-136">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="96a1d-136">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)

