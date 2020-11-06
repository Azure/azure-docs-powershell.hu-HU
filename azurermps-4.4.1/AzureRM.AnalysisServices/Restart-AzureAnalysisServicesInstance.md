---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 038c7456f849777f16ca0113d799b4ee8a16cd2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492627"
---
# <span data-ttu-id="c58dc-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="c58dc-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="c58dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c58dc-102">SYNOPSIS</span></span>
<span data-ttu-id="c58dc-103">Az Analysis Services Server példányának újraindítása az aktuálisan bejelentkezett környezetben, az Add-AzureAnalysisServicesAccount parancsban megadott módon</span><span class="sxs-lookup"><span data-stu-id="c58dc-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c58dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c58dc-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c58dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c58dc-105">DESCRIPTION</span></span>
<span data-ttu-id="c58dc-106">Az Restart-AzureAnalysisServicesInstance parancsmag az Azure Analysis Services-kiszolgáló egy példányát indítja el újra</span><span class="sxs-lookup"><span data-stu-id="c58dc-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="c58dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c58dc-107">EXAMPLES</span></span>

### <span data-ttu-id="c58dc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c58dc-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="c58dc-109">Ez a parancs elindítja a "TestServer" szervert a Add-AzureAnalysisServicesAccount parancsban megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="c58dc-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c58dc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c58dc-110">PARAMETERS</span></span>

### <span data-ttu-id="c58dc-111">-Példány</span><span class="sxs-lookup"><span data-stu-id="c58dc-111">-Instance</span></span>
<span data-ttu-id="c58dc-112">Az Analysis Services-kiszolgálópéldány újraindításának neve</span><span class="sxs-lookup"><span data-stu-id="c58dc-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58dc-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c58dc-113">-PassThru</span></span>
<span data-ttu-id="c58dc-114">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="c58dc-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c58dc-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c58dc-115">-Confirm</span></span>
<span data-ttu-id="c58dc-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c58dc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c58dc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c58dc-117">-WhatIf</span></span>
<span data-ttu-id="c58dc-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c58dc-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c58dc-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c58dc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c58dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58dc-120">CommonParameters</span></span>
<span data-ttu-id="c58dc-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c58dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58dc-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c58dc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58dc-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c58dc-123">INPUTS</span></span>

## <span data-ttu-id="c58dc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c58dc-124">OUTPUTS</span></span>

### <span data-ttu-id="c58dc-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c58dc-125">System.Boolean</span></span>

## <span data-ttu-id="c58dc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c58dc-126">NOTES</span></span>
<span data-ttu-id="c58dc-127">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="c58dc-127">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="c58dc-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c58dc-128">RELATED LINKS</span></span>

