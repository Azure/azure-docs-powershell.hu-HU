---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 348732794a0cf16233f9a139e86ed89658fc5ac2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850297"
---
# <span data-ttu-id="9a930-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9a930-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="9a930-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a930-102">SYNOPSIS</span></span>
<span data-ttu-id="9a930-103">Egy hálózati biztonsági csoport cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="9a930-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a930-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a930-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a930-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a930-105">DESCRIPTION</span></span>
<span data-ttu-id="9a930-106">A **set-AzureRmNetworkSecurityGroup** parancsmag az Azure hálózati biztonsági csoport cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="9a930-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="9a930-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9a930-107">EXAMPLES</span></span>

### <span data-ttu-id="9a930-108">Példa 1: egy hálózati biztonsági csoport cél állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="9a930-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="9a930-109">Ez a parancs beolvassa a Nsg1 nevű Azure hálózat biztonsági csoportját, és felvesz egy Rdp-Rule nevű hálózati biztonsági szabályt, amely lehetővé teszi a 3389-as porton lévő internetes forgalom engedélyezését a AzureRmNetworkSecurityRuleConfig segítségével.</span><span class="sxs-lookup"><span data-stu-id="9a930-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="9a930-110">A parancs a **set-AzureRmNetworkSecurityGroup** használatával megmarad a módosított Azure hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="9a930-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="9a930-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a930-111">PARAMETERS</span></span>

### <span data-ttu-id="9a930-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a930-112">-AsJob</span></span>
<span data-ttu-id="9a930-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9a930-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a930-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a930-114">-DefaultProfile</span></span>
<span data-ttu-id="9a930-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a930-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a930-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9a930-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9a930-117">Egy hálózati biztonsági csoport objektuma, amely annak a célnak az állapotát jelenti, amelyhez a parancsmag a hálózat biztonsági csoportját állítja be.</span><span class="sxs-lookup"><span data-stu-id="9a930-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a930-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a930-118">CommonParameters</span></span>
<span data-ttu-id="9a930-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a930-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a930-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a930-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a930-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a930-121">INPUTS</span></span>

### <span data-ttu-id="9a930-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9a930-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="9a930-123">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9a930-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="9a930-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a930-124">OUTPUTS</span></span>

### <span data-ttu-id="9a930-125">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9a930-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9a930-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a930-126">NOTES</span></span>

## <span data-ttu-id="9a930-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a930-127">RELATED LINKS</span></span>

[<span data-ttu-id="9a930-128">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9a930-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="9a930-129">Új – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9a930-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="9a930-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9a930-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


