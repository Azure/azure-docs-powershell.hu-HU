---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491892"
---
# <span data-ttu-id="116c8-101">Set-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="116c8-101">Set-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="116c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="116c8-102">SYNOPSIS</span></span>
<span data-ttu-id="116c8-103">Meglévő hálózati profilhoz tartozó célérték állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="116c8-103">Sets the goal state for an existing network profile</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="116c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="116c8-104">SYNTAX</span></span>

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="116c8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="116c8-105">DESCRIPTION</span></span>
<span data-ttu-id="116c8-106">A **set-AzureRmPublicIpPrefix** parancsmag a hálózati profil céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="116c8-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the goal state for a network profile.</span></span>

## <span data-ttu-id="116c8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="116c8-107">EXAMPLES</span></span>

### <span data-ttu-id="116c8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="116c8-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

<span data-ttu-id="116c8-109">Az első parancs a meglévő hálózati profilt kapja.</span><span class="sxs-lookup"><span data-stu-id="116c8-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="116c8-110">A második parancs frissíti a címkét, és a harmadik hozzáadja a hálózati felület konfigurációját a hálózati profilhoz.</span><span class="sxs-lookup"><span data-stu-id="116c8-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="116c8-111">A negyedik parancs frissíti a hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="116c8-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="116c8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="116c8-112">PARAMETERS</span></span>

### <span data-ttu-id="116c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="116c8-113">-AsJob</span></span>
<span data-ttu-id="116c8-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="116c8-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116c8-115">-DefaultProfile</span></span>
<span data-ttu-id="116c8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="116c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116c8-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="116c8-117">-NetworkProfile</span></span>
<span data-ttu-id="116c8-118">A hálózati profil</span><span class="sxs-lookup"><span data-stu-id="116c8-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="116c8-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="116c8-119">-Confirm</span></span>
<span data-ttu-id="116c8-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="116c8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116c8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116c8-121">-WhatIf</span></span>
<span data-ttu-id="116c8-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="116c8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116c8-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="116c8-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="116c8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116c8-124">CommonParameters</span></span>
<span data-ttu-id="116c8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="116c8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116c8-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="116c8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116c8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="116c8-127">INPUTS</span></span>

### <span data-ttu-id="116c8-128">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="116c8-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="116c8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="116c8-129">OUTPUTS</span></span>

### <span data-ttu-id="116c8-130">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="116c8-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="116c8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="116c8-131">NOTES</span></span>

## <span data-ttu-id="116c8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="116c8-132">RELATED LINKS</span></span>
