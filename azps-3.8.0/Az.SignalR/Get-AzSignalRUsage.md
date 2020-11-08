---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010787"
---
# <span data-ttu-id="0cd38-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="0cd38-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="0cd38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cd38-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd38-103">Az előfizetés használati kvótájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0cd38-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="0cd38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cd38-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cd38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cd38-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd38-106">Az előfizetés használati kvótájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0cd38-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="0cd38-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0cd38-107">EXAMPLES</span></span>

### <span data-ttu-id="0cd38-108">A használati kvóta beszerzése a hely elhelyezésével</span><span class="sxs-lookup"><span data-stu-id="0cd38-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="0cd38-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cd38-109">PARAMETERS</span></span>

### <span data-ttu-id="0cd38-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd38-110">-DefaultProfile</span></span>
<span data-ttu-id="0cd38-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cd38-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cd38-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="0cd38-112">-Location</span></span>
<span data-ttu-id="0cd38-113">A jelző szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="0cd38-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="0cd38-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd38-114">CommonParameters</span></span>
<span data-ttu-id="0cd38-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cd38-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd38-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0cd38-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd38-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cd38-117">INPUTS</span></span>

### <span data-ttu-id="0cd38-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="0cd38-118">None</span></span>

## <span data-ttu-id="0cd38-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cd38-119">OUTPUTS</span></span>

### <span data-ttu-id="0cd38-120">Microsoft. Azure. Command. Signal. models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="0cd38-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="0cd38-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cd38-121">NOTES</span></span>

## <span data-ttu-id="0cd38-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cd38-122">RELATED LINKS</span></span>
