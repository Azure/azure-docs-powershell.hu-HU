---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494245"
---
# <span data-ttu-id="838ba-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="838ba-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="838ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="838ba-102">SYNOPSIS</span></span>
<span data-ttu-id="838ba-103">Napló exportálása az Analysis Services Server egy példányáról az aktuálisan bejelentkezett környezetben, az Add-AzureAnalysisServicesAccount parancsban megadott módon</span><span class="sxs-lookup"><span data-stu-id="838ba-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="838ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="838ba-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="838ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="838ba-105">DESCRIPTION</span></span>
<span data-ttu-id="838ba-106">A Export-AzureAnalysisServicesInstance parancsmag az Azure Analysis Services-kiszolgáló egy példányára exportálja a naplót fájlba</span><span class="sxs-lookup"><span data-stu-id="838ba-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="838ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="838ba-107">EXAMPLES</span></span>

### <span data-ttu-id="838ba-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="838ba-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="838ba-109">Ez a parancs az Add-AzureAnalysisServicesAccount parancsban megadott környezetben a "TestServer" kiszolgálóról exportálja a naplót, és a OutputPath "C:\path\to\log\testserver.log" mezőben megadott fájlba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="838ba-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="838ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="838ba-110">PARAMETERS</span></span>

### <span data-ttu-id="838ba-111">-Force</span><span class="sxs-lookup"><span data-stu-id="838ba-111">-Force</span></span>
<span data-ttu-id="838ba-112">Fájl felülírása, ha a kérés nélkül létezik</span><span class="sxs-lookup"><span data-stu-id="838ba-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="838ba-113">-Példány</span><span class="sxs-lookup"><span data-stu-id="838ba-113">-Instance</span></span>
<span data-ttu-id="838ba-114">Az Analysis Services-kiszolgálópéldány neve</span><span class="sxs-lookup"><span data-stu-id="838ba-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838ba-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="838ba-115">-OutputPath</span></span>
<span data-ttu-id="838ba-116">A naplófájl exportálására szolgáló kimeneti útvonal</span><span class="sxs-lookup"><span data-stu-id="838ba-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="838ba-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="838ba-117">-Confirm</span></span>
<span data-ttu-id="838ba-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="838ba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="838ba-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="838ba-119">-WhatIf</span></span>
<span data-ttu-id="838ba-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="838ba-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="838ba-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="838ba-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="838ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838ba-122">CommonParameters</span></span>
<span data-ttu-id="838ba-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="838ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838ba-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838ba-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838ba-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="838ba-125">INPUTS</span></span>

### <span data-ttu-id="838ba-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="838ba-126">None</span></span>

## <span data-ttu-id="838ba-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="838ba-127">OUTPUTS</span></span>

### <span data-ttu-id="838ba-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="838ba-128">System.Void</span></span>

## <span data-ttu-id="838ba-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="838ba-129">NOTES</span></span>
<span data-ttu-id="838ba-130">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="838ba-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="838ba-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="838ba-131">RELATED LINKS</span></span>
