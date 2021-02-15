---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208174"
---
# <span data-ttu-id="9a6d0-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="9a6d0-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="9a6d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6d0-103">Támogatott ServiceBus-műveletek listája</span><span class="sxs-lookup"><span data-stu-id="9a6d0-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="9a6d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a6d0-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a6d0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a6d0-105">DESCRIPTION</span></span>
<span data-ttu-id="9a6d0-106">A **Get-AzServiceBusOperation** parancsmag felsorolja a ServiceBus által támogatott műveleteket.</span><span class="sxs-lookup"><span data-stu-id="9a6d0-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="9a6d0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a6d0-107">EXAMPLES</span></span>

### <span data-ttu-id="9a6d0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9a6d0-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="9a6d0-109">A ServiceBus által támogatott műveletek felsorolása</span><span class="sxs-lookup"><span data-stu-id="9a6d0-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="9a6d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a6d0-110">PARAMETERS</span></span>

### <span data-ttu-id="9a6d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6d0-111">-DefaultProfile</span></span>
<span data-ttu-id="9a6d0-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a6d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a6d0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6d0-113">CommonParameters</span></span>
<span data-ttu-id="9a6d0-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a6d0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6d0-115">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a6d0-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6d0-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a6d0-116">INPUTS</span></span>

### <span data-ttu-id="9a6d0-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="9a6d0-117">None</span></span>

## <span data-ttu-id="9a6d0-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a6d0-118">OUTPUTS</span></span>

### <span data-ttu-id="9a6d0-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="9a6d0-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="9a6d0-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a6d0-120">NOTES</span></span>

## <span data-ttu-id="9a6d0-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a6d0-121">RELATED LINKS</span></span>
