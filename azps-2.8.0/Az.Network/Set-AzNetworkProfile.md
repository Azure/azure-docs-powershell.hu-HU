---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: c63940ab03f6d288de3c1b5b0d767182168ed1fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837008"
---
# <span data-ttu-id="bcae4-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bcae4-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="bcae4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcae4-102">SYNOPSIS</span></span>
<span data-ttu-id="bcae4-103">Hálózati profil frissítése</span><span class="sxs-lookup"><span data-stu-id="bcae4-103">Updates a network profile.</span></span>

## <span data-ttu-id="bcae4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcae4-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcae4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcae4-105">DESCRIPTION</span></span>
<span data-ttu-id="bcae4-106">A **set-AzPublicIpPrefix** parancsmag hálózati profilt frissít.</span><span class="sxs-lookup"><span data-stu-id="bcae4-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="bcae4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bcae4-107">EXAMPLES</span></span>

### <span data-ttu-id="bcae4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bcae4-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="bcae4-109">Az első parancs a meglévő hálózati profilt kapja.</span><span class="sxs-lookup"><span data-stu-id="bcae4-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="bcae4-110">A második parancs frissíti a címkét, és a harmadik hozzáadja a hálózati felület konfigurációját a hálózati profilhoz.</span><span class="sxs-lookup"><span data-stu-id="bcae4-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="bcae4-111">A negyedik parancs frissíti a hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="bcae4-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="bcae4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcae4-112">PARAMETERS</span></span>

### <span data-ttu-id="bcae4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcae4-113">-AsJob</span></span>
<span data-ttu-id="bcae4-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bcae4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcae4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcae4-115">-DefaultProfile</span></span>
<span data-ttu-id="bcae4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcae4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcae4-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bcae4-117">-NetworkProfile</span></span>
<span data-ttu-id="bcae4-118">A hálózati profil</span><span class="sxs-lookup"><span data-stu-id="bcae4-118">The network profile</span></span>

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

### <span data-ttu-id="bcae4-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bcae4-119">-Confirm</span></span>
<span data-ttu-id="bcae4-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bcae4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcae4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcae4-121">-WhatIf</span></span>
<span data-ttu-id="bcae4-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bcae4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcae4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bcae4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcae4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcae4-124">CommonParameters</span></span>
<span data-ttu-id="bcae4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcae4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcae4-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcae4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcae4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcae4-127">INPUTS</span></span>

### <span data-ttu-id="bcae4-128">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bcae4-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="bcae4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcae4-129">OUTPUTS</span></span>

### <span data-ttu-id="bcae4-130">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bcae4-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="bcae4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcae4-131">NOTES</span></span>

## <span data-ttu-id="bcae4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcae4-132">RELATED LINKS</span></span>

[<span data-ttu-id="bcae4-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bcae4-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="bcae4-134">Új – AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bcae4-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="bcae4-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bcae4-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
