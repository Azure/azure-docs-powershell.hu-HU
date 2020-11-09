---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302628"
---
# <span data-ttu-id="94eb3-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="94eb3-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="94eb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="94eb3-103">A továbbítási névtérben található megadott HybridConnection leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="94eb3-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="94eb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94eb3-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94eb3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="94eb3-106">A **Get-AzRelayHybridConnection** parancsmag leírását kapja a megadott HybridConnection a továbbítási névtéren belül.</span><span class="sxs-lookup"><span data-stu-id="94eb3-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="94eb3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94eb3-107">EXAMPLES</span></span>

### <span data-ttu-id="94eb3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94eb3-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="94eb3-109">A HybridConnection leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="94eb3-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="94eb3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94eb3-110">PARAMETERS</span></span>

### <span data-ttu-id="94eb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94eb3-111">-DefaultProfile</span></span>
<span data-ttu-id="94eb3-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94eb3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94eb3-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94eb3-113">-Name</span></span>
<span data-ttu-id="94eb3-114">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="94eb3-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94eb3-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="94eb3-115">-Namespace</span></span>
<span data-ttu-id="94eb3-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="94eb3-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94eb3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94eb3-117">-ResourceGroupName</span></span>
<span data-ttu-id="94eb3-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="94eb3-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94eb3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94eb3-119">CommonParameters</span></span>
<span data-ttu-id="94eb3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94eb3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94eb3-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94eb3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94eb3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94eb3-122">INPUTS</span></span>

### <span data-ttu-id="94eb3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="94eb3-123">System.String</span></span>

## <span data-ttu-id="94eb3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94eb3-124">OUTPUTS</span></span>

### <span data-ttu-id="94eb3-125">Microsoft. Azure. Command. Relay. models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="94eb3-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="94eb3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94eb3-126">NOTES</span></span>

## <span data-ttu-id="94eb3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94eb3-127">RELATED LINKS</span></span>
