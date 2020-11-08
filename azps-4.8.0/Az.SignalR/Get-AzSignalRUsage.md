---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017586"
---
# <span data-ttu-id="52bf1-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="52bf1-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="52bf1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="52bf1-103">Az előfizetés használati kvótájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="52bf1-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="52bf1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52bf1-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52bf1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="52bf1-105">DESCRIPTION</span></span>
<span data-ttu-id="52bf1-106">Az előfizetés használati kvótájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="52bf1-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="52bf1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="52bf1-107">EXAMPLES</span></span>

### <span data-ttu-id="52bf1-108">A használati kvóta beszerzése a hely elhelyezésével</span><span class="sxs-lookup"><span data-stu-id="52bf1-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="52bf1-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52bf1-109">PARAMETERS</span></span>

### <span data-ttu-id="52bf1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bf1-110">-DefaultProfile</span></span>
<span data-ttu-id="52bf1-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52bf1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52bf1-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="52bf1-112">-Location</span></span>
<span data-ttu-id="52bf1-113">A jelző szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="52bf1-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="52bf1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bf1-114">CommonParameters</span></span>
<span data-ttu-id="52bf1-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52bf1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52bf1-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="52bf1-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bf1-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52bf1-117">INPUTS</span></span>

### <span data-ttu-id="52bf1-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="52bf1-118">None</span></span>

## <span data-ttu-id="52bf1-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52bf1-119">OUTPUTS</span></span>

### <span data-ttu-id="52bf1-120">Microsoft. Azure. Command. Signal. models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="52bf1-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="52bf1-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52bf1-121">NOTES</span></span>

## <span data-ttu-id="52bf1-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52bf1-122">RELATED LINKS</span></span>
