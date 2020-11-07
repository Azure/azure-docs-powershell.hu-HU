---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680781"
---
# <span data-ttu-id="ca56b-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="ca56b-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="ca56b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca56b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca56b-103">Napló exportálása az Analysis Services Server egy példányáról az aktuálisan bejelentkezett környezetben, az Add-AzureAnalysisServicesAccount parancsban megadott módon</span><span class="sxs-lookup"><span data-stu-id="ca56b-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca56b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca56b-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="ca56b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca56b-105">DESCRIPTION</span></span>
<span data-ttu-id="ca56b-106">A Export-AzureAnalysisServicesInstance parancsmag az Azure Analysis Services-kiszolgáló egy példányára exportálja a naplót fájlba</span><span class="sxs-lookup"><span data-stu-id="ca56b-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="ca56b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca56b-107">EXAMPLES</span></span>

### <span data-ttu-id="ca56b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca56b-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="ca56b-109">Ez a parancs az Add-AzureAnalysisServicesAccount parancsban megadott környezetben a "TestServer" kiszolgálóról exportálja a naplót, és a OutputPath "C:\path\to\log\testserver.log" mezőben megadott fájlba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="ca56b-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="ca56b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca56b-110">PARAMETERS</span></span>

### <span data-ttu-id="ca56b-111">-Példány</span><span class="sxs-lookup"><span data-stu-id="ca56b-111">-Instance</span></span>
<span data-ttu-id="ca56b-112">Az Analysis Services-kiszolgálópéldány neve</span><span class="sxs-lookup"><span data-stu-id="ca56b-112">Name of the Analysis Services server instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca56b-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="ca56b-113">-OutputPath</span></span>
<span data-ttu-id="ca56b-114">A naplófájl exportálására szolgáló kimeneti útvonal</span><span class="sxs-lookup"><span data-stu-id="ca56b-114">Output path to file to export log</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca56b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca56b-115">-Force</span></span>
<span data-ttu-id="ca56b-116">Fájl felülírása, ha a kérés nélkül létezik</span><span class="sxs-lookup"><span data-stu-id="ca56b-116">Overwrite file if exists without asking</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="ca56b-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca56b-117">INPUTS</span></span>

## <span data-ttu-id="ca56b-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca56b-118">OUTPUTS</span></span>

## <span data-ttu-id="ca56b-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca56b-119">NOTES</span></span>
<span data-ttu-id="ca56b-120">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="ca56b-120">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="ca56b-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca56b-121">RELATED LINKS</span></span>

