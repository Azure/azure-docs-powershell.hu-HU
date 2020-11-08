---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013073"
---
# <span data-ttu-id="99273-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="99273-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="99273-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99273-102">SYNOPSIS</span></span>
<span data-ttu-id="99273-103">Támogatott ServiceBus-műveletek listája</span><span class="sxs-lookup"><span data-stu-id="99273-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="99273-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99273-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99273-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99273-105">DESCRIPTION</span></span>
<span data-ttu-id="99273-106">A **Get-AzServiceBusOperation** parancsmag a támogatott ServiceBus-műveleteket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="99273-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="99273-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99273-107">EXAMPLES</span></span>

### <span data-ttu-id="99273-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99273-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="99273-109">A ServiceBus által támogatott műveletek listája</span><span class="sxs-lookup"><span data-stu-id="99273-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="99273-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99273-110">PARAMETERS</span></span>

### <span data-ttu-id="99273-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99273-111">-DefaultProfile</span></span>
<span data-ttu-id="99273-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99273-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99273-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99273-113">CommonParameters</span></span>
<span data-ttu-id="99273-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99273-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99273-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99273-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99273-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99273-116">INPUTS</span></span>

### <span data-ttu-id="99273-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="99273-117">None</span></span>

## <span data-ttu-id="99273-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99273-118">OUTPUTS</span></span>

### <span data-ttu-id="99273-119">Microsoft. Azure. Command. ServiceBus. models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="99273-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="99273-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99273-120">NOTES</span></span>

## <span data-ttu-id="99273-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99273-121">RELATED LINKS</span></span>
