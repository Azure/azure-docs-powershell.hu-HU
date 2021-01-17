---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 21bf1e235d9e6b2f6bb4d2017b69f607e559e46b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466585"
---
# <span data-ttu-id="bbd1b-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="bbd1b-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="bbd1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd1b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd1b-103">Támogatott továbbítási műveletek listája</span><span class="sxs-lookup"><span data-stu-id="bbd1b-103">List supported Relay Operations</span></span>

## <span data-ttu-id="bbd1b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bbd1b-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbd1b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bbd1b-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd1b-106">A **Get-AzRelayOperation** parancsmag felsorolja a továbbító által támogatott műveleteket.</span><span class="sxs-lookup"><span data-stu-id="bbd1b-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="bbd1b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bbd1b-107">EXAMPLES</span></span>

### <span data-ttu-id="bbd1b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="bbd1b-108">Example 1</span></span>
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

<span data-ttu-id="bbd1b-109">A Továbbítás támogatott műveleteinek felsorolása</span><span class="sxs-lookup"><span data-stu-id="bbd1b-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="bbd1b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbd1b-110">PARAMETERS</span></span>

### <span data-ttu-id="bbd1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd1b-111">-DefaultProfile</span></span>
<span data-ttu-id="bbd1b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbd1b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd1b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd1b-113">CommonParameters</span></span>
<span data-ttu-id="bbd1b-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd1b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd1b-115">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd1b-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd1b-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbd1b-116">INPUTS</span></span>

### <span data-ttu-id="bbd1b-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="bbd1b-117">None</span></span>

## <span data-ttu-id="bbd1b-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbd1b-118">OUTPUTS</span></span>

### <span data-ttu-id="bbd1b-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="bbd1b-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="bbd1b-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bbd1b-120">NOTES</span></span>

## <span data-ttu-id="bbd1b-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbd1b-121">RELATED LINKS</span></span>
