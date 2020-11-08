---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186541"
---
# <span data-ttu-id="07ffc-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="07ffc-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="07ffc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="07ffc-103">Támogatott ServiceBus-műveletek listája</span><span class="sxs-lookup"><span data-stu-id="07ffc-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="07ffc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07ffc-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ffc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="07ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="07ffc-106">A **Get-AzServiceBusOperation** parancsmag a támogatott ServiceBus-műveleteket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="07ffc-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="07ffc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="07ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="07ffc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07ffc-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="07ffc-109">A ServiceBus által támogatott műveletek listája</span><span class="sxs-lookup"><span data-stu-id="07ffc-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="07ffc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07ffc-110">PARAMETERS</span></span>

### <span data-ttu-id="07ffc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ffc-111">-DefaultProfile</span></span>
<span data-ttu-id="07ffc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07ffc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07ffc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ffc-113">CommonParameters</span></span>
<span data-ttu-id="07ffc-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07ffc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ffc-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ffc-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ffc-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07ffc-116">INPUTS</span></span>

### <span data-ttu-id="07ffc-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="07ffc-117">None</span></span>

## <span data-ttu-id="07ffc-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07ffc-118">OUTPUTS</span></span>

### <span data-ttu-id="07ffc-119">Microsoft. Azure. Command. ServiceBus. models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="07ffc-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="07ffc-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07ffc-120">NOTES</span></span>

## <span data-ttu-id="07ffc-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07ffc-121">RELATED LINKS</span></span>