---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: ab009608100bc4cbb4915f6bc3e82d44d9e08cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679878"
---
# <span data-ttu-id="528e9-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="528e9-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="528e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="528e9-102">SYNOPSIS</span></span>
<span data-ttu-id="528e9-103">Egy hálózati biztonsági csoport cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="528e9-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="528e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="528e9-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="528e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="528e9-105">DESCRIPTION</span></span>
<span data-ttu-id="528e9-106">A **set-AzureRmNetworkSecurityGroup** parancsmag az Azure hálózati biztonsági csoport cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="528e9-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="528e9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="528e9-107">EXAMPLES</span></span>

### <span data-ttu-id="528e9-108">Példa 1: egy hálózati biztonsági csoport cél állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="528e9-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="528e9-109">Ez a parancs beolvassa a Nsg1 nevű Azure hálózat biztonsági csoportját, és felvesz egy Rdp-Rule nevű hálózati biztonsági szabályt, amely lehetővé teszi a 3389-as porton lévő internetes forgalom engedélyezését a AzureRmNetworkSecurityRuleConfig segítségével.</span><span class="sxs-lookup"><span data-stu-id="528e9-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="528e9-110">A parancs a **set-AzureRmNetworkSecurityGroup** használatával megmarad a módosított Azure hálózat biztonsági csoportja.</span><span class="sxs-lookup"><span data-stu-id="528e9-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="528e9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="528e9-111">PARAMETERS</span></span>

### <span data-ttu-id="528e9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="528e9-112">-AsJob</span></span>
<span data-ttu-id="528e9-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="528e9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="528e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="528e9-114">-DefaultProfile</span></span>
<span data-ttu-id="528e9-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="528e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="528e9-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="528e9-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="528e9-117">Egy hálózati biztonsági csoport objektuma, amely annak a célnak az állapotát jelenti, amelyhez a parancsmag a hálózat biztonsági csoportját állítja be.</span><span class="sxs-lookup"><span data-stu-id="528e9-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="528e9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="528e9-118">CommonParameters</span></span>
<span data-ttu-id="528e9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="528e9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="528e9-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="528e9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="528e9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="528e9-121">INPUTS</span></span>

### <span data-ttu-id="528e9-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="528e9-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="528e9-123">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="528e9-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="528e9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="528e9-124">OUTPUTS</span></span>

### <span data-ttu-id="528e9-125">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="528e9-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="528e9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="528e9-126">NOTES</span></span>

## <span data-ttu-id="528e9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="528e9-127">RELATED LINKS</span></span>

[<span data-ttu-id="528e9-128">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="528e9-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="528e9-129">Új – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="528e9-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="528e9-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="528e9-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


