---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494806"
---
# <span data-ttu-id="78e93-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78e93-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="78e93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78e93-102">SYNOPSIS</span></span>
<span data-ttu-id="78e93-103">Egy hálózati biztonsági csoport cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="78e93-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78e93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78e93-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78e93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78e93-105">DESCRIPTION</span></span>
<span data-ttu-id="78e93-106">A **set-AzureRmNetworkSecurityGroup** parancsmag az Azure hálózati biztonsági csoport cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="78e93-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="78e93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="78e93-107">EXAMPLES</span></span>

### <span data-ttu-id="78e93-108">Példa 1: egy hálózati biztonsági csoport cél állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="78e93-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="78e93-109">Ez a parancs beolvassa a Nsg1 nevű Azure hálózat biztonsági csoportját, és felvesz egy Rdp-Rule nevű hálózati biztonsági szabályt, amely lehetővé teszi a 3389-as porton lévő internetes forgalom engedélyezését a AzureRmNetworkSecurityRuleConfig segítségével.</span><span class="sxs-lookup"><span data-stu-id="78e93-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="78e93-110">A parancs a **set-AzureRmNetworkSecurityGroup** használatával megmarad a módosított Azure hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="78e93-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="78e93-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78e93-111">PARAMETERS</span></span>

### <span data-ttu-id="78e93-112">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78e93-112">-NetworkSecurityGroup</span></span>
<span data-ttu-id="78e93-113">Egy hálózati biztonsági csoport objektuma, amely annak a célnak az állapotát jelenti, amelyhez a parancsmag a hálózat biztonsági csoportját állítja be.</span><span class="sxs-lookup"><span data-stu-id="78e93-113">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78e93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e93-114">-DefaultProfile</span></span>
<span data-ttu-id="78e93-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78e93-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78e93-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e93-116">CommonParameters</span></span>
<span data-ttu-id="78e93-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78e93-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e93-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78e93-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e93-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78e93-119">INPUTS</span></span>

### <span data-ttu-id="78e93-120">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78e93-120">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="78e93-121">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="78e93-121">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="78e93-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78e93-122">OUTPUTS</span></span>

### <span data-ttu-id="78e93-123">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78e93-123">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="78e93-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78e93-124">NOTES</span></span>

## <span data-ttu-id="78e93-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78e93-125">RELATED LINKS</span></span>

[<span data-ttu-id="78e93-126">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78e93-126">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="78e93-127">Új – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78e93-127">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="78e93-128">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78e93-128">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


