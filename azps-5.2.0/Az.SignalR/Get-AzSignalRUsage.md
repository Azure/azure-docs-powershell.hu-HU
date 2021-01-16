---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356358"
---
# <span data-ttu-id="9df67-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="9df67-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="9df67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9df67-102">SYNOPSIS</span></span>
<span data-ttu-id="9df67-103">Előfizetés használati kvótáját is lekérte.</span><span class="sxs-lookup"><span data-stu-id="9df67-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="9df67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9df67-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9df67-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9df67-105">DESCRIPTION</span></span>
<span data-ttu-id="9df67-106">Előfizetés használati kvótáját is lekérte.</span><span class="sxs-lookup"><span data-stu-id="9df67-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="9df67-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9df67-107">EXAMPLES</span></span>

### <span data-ttu-id="9df67-108">A használati kvóta lekérte a hely bevitelével</span><span class="sxs-lookup"><span data-stu-id="9df67-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="9df67-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9df67-109">PARAMETERS</span></span>

### <span data-ttu-id="9df67-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df67-110">-DefaultProfile</span></span>
<span data-ttu-id="9df67-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9df67-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9df67-112">-Location</span><span class="sxs-lookup"><span data-stu-id="9df67-112">-Location</span></span>
<span data-ttu-id="9df67-113">A SignalR szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="9df67-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="9df67-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df67-114">CommonParameters</span></span>
<span data-ttu-id="9df67-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9df67-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df67-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9df67-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df67-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9df67-117">INPUTS</span></span>

### <span data-ttu-id="9df67-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="9df67-118">None</span></span>

## <span data-ttu-id="9df67-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9df67-119">OUTPUTS</span></span>

### <span data-ttu-id="9df67-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="9df67-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="9df67-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9df67-121">NOTES</span></span>

## <span data-ttu-id="9df67-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9df67-122">RELATED LINKS</span></span>
