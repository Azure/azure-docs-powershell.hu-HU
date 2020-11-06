---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
ms.openlocfilehash: e7f45be6a39cdd2b7f2d11736d2a5f62831244c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494964"
---
# <span data-ttu-id="5afde-101">Get-AzureRmRelayOperation</span><span class="sxs-lookup"><span data-stu-id="5afde-101">Get-AzureRmRelayOperation</span></span>

## <span data-ttu-id="5afde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5afde-102">SYNOPSIS</span></span>
<span data-ttu-id="5afde-103">Támogatott továbbító műveletek listája</span><span class="sxs-lookup"><span data-stu-id="5afde-103">List supported Relay Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5afde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5afde-104">SYNTAX</span></span>

```
Get-AzureRmRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5afde-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5afde-105">DESCRIPTION</span></span>
<span data-ttu-id="5afde-106">A **Get-AzureRmRelayOperation** parancsmag felsorolja a továbbító által támogatott műveleteket.</span><span class="sxs-lookup"><span data-stu-id="5afde-106">The **Get-AzureRmRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="5afde-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5afde-107">EXAMPLES</span></span>

### <span data-ttu-id="5afde-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5afde-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayOperation

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

<span data-ttu-id="5afde-109">A továbbító által támogatott műveletek listája</span><span class="sxs-lookup"><span data-stu-id="5afde-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="5afde-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5afde-110">PARAMETERS</span></span>

### <span data-ttu-id="5afde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5afde-111">-DefaultProfile</span></span>
<span data-ttu-id="5afde-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5afde-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afde-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5afde-113">CommonParameters</span></span>
<span data-ttu-id="5afde-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5afde-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5afde-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5afde-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5afde-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5afde-116">INPUTS</span></span>

### <span data-ttu-id="5afde-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="5afde-117">None</span></span>


## <span data-ttu-id="5afde-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5afde-118">OUTPUTS</span></span>

### <span data-ttu-id="5afde-119">Microsoft. Azure. Command. Relay. models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="5afde-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>


## <span data-ttu-id="5afde-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5afde-120">NOTES</span></span>

## <span data-ttu-id="5afde-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5afde-121">RELATED LINKS</span></span>
