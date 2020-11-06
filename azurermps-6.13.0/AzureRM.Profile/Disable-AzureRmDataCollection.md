---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 751dc5f8d75a498f843ebd7e543503c871cad1c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504295"
---
# <span data-ttu-id="c1315-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="c1315-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="c1315-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1315-102">SYNOPSIS</span></span>
<span data-ttu-id="c1315-103">A AzurePowerShell-parancsmagok fejlesztéséhez kimarad az adatok gyűjtése.</span><span class="sxs-lookup"><span data-stu-id="c1315-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="c1315-104">Az adatokat csak akkor gyűjti össze, ha kifejezetten bejelöli.</span><span class="sxs-lookup"><span data-stu-id="c1315-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1315-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1315-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1315-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1315-106">DESCRIPTION</span></span>
<span data-ttu-id="c1315-107">Javíthatja a Microsoft Cloud és az Azure PowerShell használatával kapcsolatos tapasztalatokat az adatgyűjtés kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="c1315-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="c1315-108">Az Azure PowerShell nem gyűjti össze az adatokat a hozzájárulása nélkül – az engedélyezés – AzureRmDataCollection, vagy ha az Azure PowerShell kéri az adatok gyűjtését a parancsmag első futtatásakor.</span><span class="sxs-lookup"><span data-stu-id="c1315-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="c1315-109">A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére és az Azure PowerShell használatba vétele érdekében.</span><span class="sxs-lookup"><span data-stu-id="c1315-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="c1315-110">A Microsoft Azure PowerShell semmilyen személyes adatot nem gyűjt, vagy bármilyen személyazonosításra alkalmas információt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c1315-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="c1315-111">A Disable-AzureRMDataCollection parancsmag futtatásával tiltsa le az aktuális felhasználó adatgyűjtési szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="c1315-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="c1315-112">Ez megakadályozza, hogy az aktuális felhasználó Kérdezzen az adatgyűjtésről az első időparancsmagok végrehajtása során.</span><span class="sxs-lookup"><span data-stu-id="c1315-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="c1315-113">Ha engedélyezni szeretné a jelenlegi felhasználó adatgyűjtését, futtassa az Enable-AzureRmDataCollection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c1315-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="c1315-114">Példák</span><span class="sxs-lookup"><span data-stu-id="c1315-114">EXAMPLES</span></span>

### <span data-ttu-id="c1315-115">1. példa: az aktuális felhasználó adatgyűjtésének letiltása</span><span class="sxs-lookup"><span data-stu-id="c1315-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="c1315-116">Ez a példa bemutatja, hogyan tilthatja le az aktuális felhasználó adatgyűjtését.</span><span class="sxs-lookup"><span data-stu-id="c1315-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="c1315-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1315-117">PARAMETERS</span></span>

### <span data-ttu-id="c1315-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1315-118">-DefaultProfile</span></span>
<span data-ttu-id="c1315-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1315-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1315-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1315-120">-Confirm</span></span>
<span data-ttu-id="c1315-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1315-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1315-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1315-122">-WhatIf</span></span>
<span data-ttu-id="c1315-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1315-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1315-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1315-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1315-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1315-125">CommonParameters</span></span>
<span data-ttu-id="c1315-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1315-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1315-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1315-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1315-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1315-128">INPUTS</span></span>

### <span data-ttu-id="c1315-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="c1315-129">None</span></span>

## <span data-ttu-id="c1315-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1315-130">OUTPUTS</span></span>

### <span data-ttu-id="c1315-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="c1315-131">System.Void</span></span>

## <span data-ttu-id="c1315-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1315-132">NOTES</span></span>

## <span data-ttu-id="c1315-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1315-133">RELATED LINKS</span></span>

[<span data-ttu-id="c1315-134">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="c1315-134">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

