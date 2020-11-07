---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843613"
---
# <span data-ttu-id="0a019-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a019-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="0a019-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a019-102">SYNOPSIS</span></span>
<span data-ttu-id="0a019-103">Egy hálózati biztonsági csoport cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="0a019-103">Sets the goal state for a network security group.</span></span>

## <span data-ttu-id="0a019-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a019-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a019-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a019-105">DESCRIPTION</span></span>
<span data-ttu-id="0a019-106">A **set-AzNetworkSecurityGroup** parancsmag az Azure hálózati biztonsági csoport cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="0a019-106">The **Set-AzNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="0a019-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0a019-107">EXAMPLES</span></span>

### <span data-ttu-id="0a019-108">Példa 1: egy hálózati biztonsági csoport cél állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="0a019-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="0a019-109">Ez a parancs beolvassa a Nsg1 nevű Azure hálózat biztonsági csoportját, és felvesz egy Rdp-Rule nevű hálózati biztonsági szabályt, amely lehetővé teszi a 3389-as porton lévő internetes forgalom engedélyezését a AzNetworkSecurityRuleConfig segítségével.</span><span class="sxs-lookup"><span data-stu-id="0a019-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="0a019-110">A parancs a **set-AzNetworkSecurityGroup** használatával megmarad a módosított Azure hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="0a019-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="0a019-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a019-111">PARAMETERS</span></span>

### <span data-ttu-id="0a019-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a019-112">-AsJob</span></span>
<span data-ttu-id="0a019-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0a019-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a019-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a019-114">-DefaultProfile</span></span>
<span data-ttu-id="0a019-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a019-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a019-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a019-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0a019-117">Egy hálózati biztonsági csoport objektuma, amely annak a célnak az állapotát jelenti, amelyhez a parancsmag a hálózat biztonsági csoportját állítja be.</span><span class="sxs-lookup"><span data-stu-id="0a019-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="0a019-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a019-118">CommonParameters</span></span>
<span data-ttu-id="0a019-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a019-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a019-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a019-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a019-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a019-121">INPUTS</span></span>

### <span data-ttu-id="0a019-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a019-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="0a019-123">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0a019-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="0a019-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a019-124">OUTPUTS</span></span>

### <span data-ttu-id="0a019-125">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a019-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0a019-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a019-126">NOTES</span></span>

## <span data-ttu-id="0a019-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a019-127">RELATED LINKS</span></span>

[<span data-ttu-id="0a019-128">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a019-128">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="0a019-129">Új – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a019-129">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="0a019-130">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a019-130">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


