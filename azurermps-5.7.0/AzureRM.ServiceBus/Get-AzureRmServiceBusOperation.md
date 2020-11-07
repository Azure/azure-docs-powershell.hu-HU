---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: de2e826223520c13306411c5d52f448468186804
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679703"
---
# <span data-ttu-id="66b25-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="66b25-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="66b25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66b25-102">SYNOPSIS</span></span>
<span data-ttu-id="66b25-103">Támogatott ServiceBus-műveletek listája</span><span class="sxs-lookup"><span data-stu-id="66b25-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66b25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66b25-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66b25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66b25-105">DESCRIPTION</span></span>
<span data-ttu-id="66b25-106">A **Get-AzureRmServiceBusOperation** parancsmag a támogatott ServiceBus-műveleteket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="66b25-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="66b25-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66b25-107">EXAMPLES</span></span>

### <span data-ttu-id="66b25-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="66b25-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="66b25-109">A ServiceBus által támogatott műveletek listája</span><span class="sxs-lookup"><span data-stu-id="66b25-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="66b25-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66b25-110">PARAMETERS</span></span>

### <span data-ttu-id="66b25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b25-111">-DefaultProfile</span></span>
<span data-ttu-id="66b25-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66b25-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b25-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b25-113">CommonParameters</span></span>
<span data-ttu-id="66b25-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66b25-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b25-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b25-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b25-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66b25-116">INPUTS</span></span>

### <span data-ttu-id="66b25-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="66b25-117">None</span></span>

### <span data-ttu-id="66b25-118">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. PSOperationAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.4.2.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="66b25-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="66b25-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66b25-119">OUTPUTS</span></span>

### <span data-ttu-id="66b25-120">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ServiceBus. models. OperationAttributes]</span><span class="sxs-lookup"><span data-stu-id="66b25-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="66b25-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66b25-121">NOTES</span></span>

## <span data-ttu-id="66b25-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66b25-122">RELATED LINKS</span></span>

