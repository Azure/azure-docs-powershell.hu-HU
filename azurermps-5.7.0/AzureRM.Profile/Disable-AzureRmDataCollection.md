---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 07b541636229d65a092dc9a3067d3a4cef89cac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502547"
---
# <span data-ttu-id="6b686-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="6b686-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="6b686-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b686-102">SYNOPSIS</span></span>
<span data-ttu-id="6b686-103">A AzurePowerShell-parancsmagok fejlesztéséhez kimarad az adatok gyűjtése.</span><span class="sxs-lookup"><span data-stu-id="6b686-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="6b686-104">Az adatokat csak akkor gyűjti össze, ha kifejezetten bejelöli.</span><span class="sxs-lookup"><span data-stu-id="6b686-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b686-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b686-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b686-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b686-106">DESCRIPTION</span></span>
<span data-ttu-id="6b686-107">Javíthatja a Microsoft Cloud és az Azure PowerShell használatával kapcsolatos tapasztalatokat az adatgyűjtés kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="6b686-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="6b686-108">Az Azure PowerShell nem gyűjti össze az adatokat a hozzájárulása nélkül – az engedélyezés – AzureRmDataCollection, vagy ha az Azure PowerShell kéri az adatok gyűjtését a parancsmag első futtatásakor.</span><span class="sxs-lookup"><span data-stu-id="6b686-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="6b686-109">A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére és az Azure PowerShell használatba vétele érdekében.</span><span class="sxs-lookup"><span data-stu-id="6b686-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="6b686-110">A Microsoft Azure PowerShell semmilyen személyes adatot nem gyűjt, vagy bármilyen személyazonosításra alkalmas információt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6b686-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="6b686-111">A Disable-AzureRMDataCollection parancsmag futtatásával tiltsa le az aktuális felhasználó adatgyűjtési szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="6b686-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="6b686-112">Ez megakadályozza, hogy az aktuális felhasználó Kérdezzen az adatgyűjtésről az első időparancsmagok végrehajtása során.</span><span class="sxs-lookup"><span data-stu-id="6b686-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="6b686-113">Ha engedélyezni szeretné a jelenlegi felhasználó adatgyűjtését, futtassa az Enable-AzureRmDataCollection parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6b686-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="6b686-114">Példák</span><span class="sxs-lookup"><span data-stu-id="6b686-114">EXAMPLES</span></span>

### <span data-ttu-id="6b686-115">1. példa: az aktuális felhasználó adatgyűjtésének letiltása</span><span class="sxs-lookup"><span data-stu-id="6b686-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="6b686-116">Ez a példa bemutatja, hogyan tilthatja le az aktuális felhasználó adatgyűjtését.</span><span class="sxs-lookup"><span data-stu-id="6b686-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="6b686-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b686-117">PARAMETERS</span></span>

### <span data-ttu-id="6b686-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b686-118">-DefaultProfile</span></span>
<span data-ttu-id="6b686-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b686-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b686-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6b686-120">-Confirm</span></span>
<span data-ttu-id="6b686-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b686-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b686-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b686-122">-WhatIf</span></span>
<span data-ttu-id="6b686-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6b686-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b686-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b686-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b686-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b686-125">CommonParameters</span></span>
<span data-ttu-id="6b686-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b686-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b686-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b686-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b686-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b686-128">INPUTS</span></span>

### <span data-ttu-id="6b686-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="6b686-129">None</span></span>
<span data-ttu-id="6b686-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6b686-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b686-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b686-131">OUTPUTS</span></span>

### <span data-ttu-id="6b686-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="6b686-132">None</span></span>

## <span data-ttu-id="6b686-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b686-133">NOTES</span></span>

## <span data-ttu-id="6b686-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b686-134">RELATED LINKS</span></span>

[<span data-ttu-id="6b686-135">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="6b686-135">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)
