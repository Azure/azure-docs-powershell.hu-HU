---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 468128f16c3a5ef7ef4b400694dbcc1c570f5488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505284"
---
# <span data-ttu-id="996e8-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="996e8-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="996e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="996e8-102">SYNOPSIS</span></span>
<span data-ttu-id="996e8-103">A továbbítási névtérben található megadott HybridConnection leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="996e8-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="996e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="996e8-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="996e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="996e8-105">DESCRIPTION</span></span>
<span data-ttu-id="996e8-106">A **Get-AzureRmRelayHybridConnection** parancsmag leírását kapja a megadott HybridConnection a továbbítási névtéren belül.</span><span class="sxs-lookup"><span data-stu-id="996e8-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="996e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="996e8-107">EXAMPLES</span></span>

### <span data-ttu-id="996e8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="996e8-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

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

<span data-ttu-id="996e8-109">A HybridConnection leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="996e8-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="996e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="996e8-110">PARAMETERS</span></span>

### <span data-ttu-id="996e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996e8-111">-DefaultProfile</span></span>
<span data-ttu-id="996e8-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="996e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="996e8-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="996e8-113">-Name</span></span>
<span data-ttu-id="996e8-114">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="996e8-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="996e8-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="996e8-115">-Namespace</span></span>
<span data-ttu-id="996e8-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="996e8-116">Namespace Name.</span></span>

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

### <span data-ttu-id="996e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="996e8-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="996e8-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="996e8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996e8-119">CommonParameters</span></span>
<span data-ttu-id="996e8-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="996e8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="996e8-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="996e8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996e8-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="996e8-122">INPUTS</span></span>

### <span data-ttu-id="996e8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="996e8-123">System.String</span></span>


## <span data-ttu-id="996e8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="996e8-124">OUTPUTS</span></span>

### <span data-ttu-id="996e8-125">Microsoft. Azure. Command. Relay. models. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="996e8-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="996e8-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="996e8-126">NOTES</span></span>

## <span data-ttu-id="996e8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="996e8-127">RELATED LINKS</span></span>
