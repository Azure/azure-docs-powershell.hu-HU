---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 21bf1e235d9e6b2f6bb4d2017b69f607e559e46b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181444"
---
# <span data-ttu-id="30154-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="30154-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="30154-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30154-102">SYNOPSIS</span></span>
<span data-ttu-id="30154-103">Támogatott továbbító műveletek listája</span><span class="sxs-lookup"><span data-stu-id="30154-103">List supported Relay Operations</span></span>

## <span data-ttu-id="30154-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30154-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30154-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30154-105">DESCRIPTION</span></span>
<span data-ttu-id="30154-106">A **Get-AzRelayOperation** parancsmag felsorolja a továbbító által támogatott műveleteket.</span><span class="sxs-lookup"><span data-stu-id="30154-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="30154-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30154-107">EXAMPLES</span></span>

### <span data-ttu-id="30154-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="30154-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="30154-109">A továbbító által támogatott műveletek listája</span><span class="sxs-lookup"><span data-stu-id="30154-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="30154-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30154-110">PARAMETERS</span></span>

### <span data-ttu-id="30154-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30154-111">-DefaultProfile</span></span>
<span data-ttu-id="30154-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30154-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30154-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30154-113">CommonParameters</span></span>
<span data-ttu-id="30154-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30154-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30154-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30154-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30154-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30154-116">INPUTS</span></span>

### <span data-ttu-id="30154-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="30154-117">None</span></span>

## <span data-ttu-id="30154-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30154-118">OUTPUTS</span></span>

### <span data-ttu-id="30154-119">Microsoft. Azure. Command. Relay. models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="30154-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="30154-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30154-120">NOTES</span></span>

## <span data-ttu-id="30154-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30154-121">RELATED LINKS</span></span>
