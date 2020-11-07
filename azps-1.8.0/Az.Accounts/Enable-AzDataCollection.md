---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665805"
---
# <span data-ttu-id="01ff9-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="01ff9-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="01ff9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="01ff9-103">Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="01ff9-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="01ff9-104">A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.</span><span class="sxs-lookup"><span data-stu-id="01ff9-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="01ff9-105">Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.</span><span class="sxs-lookup"><span data-stu-id="01ff9-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="01ff9-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01ff9-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01ff9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="01ff9-107">DESCRIPTION</span></span>
<span data-ttu-id="01ff9-108">Javíthatja a Microsoft Cloud és az Azure PowerShell használatával kapcsolatos tapasztalatokat az adatgyűjtés kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="01ff9-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="01ff9-109">Az Azure PowerShell nem gyűjti össze az adatokat a hozzájárulása nélkül – az engedélyezés – AzDataCollection, vagy ha az Azure PowerShell kéri az adatok gyűjtését a parancsmag első futtatásakor.</span><span class="sxs-lookup"><span data-stu-id="01ff9-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="01ff9-110">A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére és az Azure PowerShell használatba vétele érdekében.</span><span class="sxs-lookup"><span data-stu-id="01ff9-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="01ff9-111">A Microsoft Azure PowerShell semmilyen személyes adatot nem gyűjt, vagy bármilyen személyazonosításra alkalmas információt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="01ff9-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="01ff9-112">Futtassa az Enable-AzDataCollection parancsmagot az aktuális számítógépen az aktuális felhasználó adatgyűjtése engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="01ff9-112">Run the Enable-AzDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="01ff9-113">Ez megakadályozza, hogy az aktuális felhasználó Kérdezzen az adatgyűjtésről az első időparancsmagok végrehajtása során.</span><span class="sxs-lookup"><span data-stu-id="01ff9-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="01ff9-114">Az aktuális felhasználó adatgyűjtésének letiltásához futtassa az Disable-AzDataCollection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="01ff9-114">To disable data collection for the current user, run the Disable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="01ff9-115">Példák</span><span class="sxs-lookup"><span data-stu-id="01ff9-115">EXAMPLES</span></span>

### <span data-ttu-id="01ff9-116">1. példa: adatgyűjtés engedélyezése az aktuális felhasználónál</span><span class="sxs-lookup"><span data-stu-id="01ff9-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzDataCollection
```

<span data-ttu-id="01ff9-117">Ebben a példában bemutatjuk, hogy miként engedélyezheti az aktuális felhasználó adatgyűjtését.</span><span class="sxs-lookup"><span data-stu-id="01ff9-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="01ff9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01ff9-118">PARAMETERS</span></span>

### <span data-ttu-id="01ff9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ff9-119">-DefaultProfile</span></span>
<span data-ttu-id="01ff9-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01ff9-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01ff9-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="01ff9-121">-Confirm</span></span>
<span data-ttu-id="01ff9-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="01ff9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01ff9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ff9-123">-WhatIf</span></span>
<span data-ttu-id="01ff9-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="01ff9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01ff9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01ff9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01ff9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ff9-126">CommonParameters</span></span>
<span data-ttu-id="01ff9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01ff9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ff9-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ff9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ff9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01ff9-129">INPUTS</span></span>

### <span data-ttu-id="01ff9-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="01ff9-130">None</span></span>

## <span data-ttu-id="01ff9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01ff9-131">OUTPUTS</span></span>

### <span data-ttu-id="01ff9-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="01ff9-132">System.Void</span></span>

## <span data-ttu-id="01ff9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01ff9-133">NOTES</span></span>

## <span data-ttu-id="01ff9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01ff9-134">RELATED LINKS</span></span>

[<span data-ttu-id="01ff9-135">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="01ff9-135">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)

