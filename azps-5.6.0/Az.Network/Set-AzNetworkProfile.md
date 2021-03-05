---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: 5cb8c8f93b491476e01d5ae54cf2db93ac4a848a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003318"
---
# <span data-ttu-id="dd754-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd754-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="dd754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd754-102">SYNOPSIS</span></span>
<span data-ttu-id="dd754-103">Frissíti a hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="dd754-103">Updates a network profile.</span></span>

## <span data-ttu-id="dd754-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd754-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd754-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd754-105">DESCRIPTION</span></span>
<span data-ttu-id="dd754-106">A **Set-AzPublicIpPrefix** parancsmag frissíti a hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="dd754-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="dd754-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd754-107">EXAMPLES</span></span>

### <span data-ttu-id="dd754-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="dd754-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="dd754-109">Az első parancs egy meglévő hálózati profilt kap.</span><span class="sxs-lookup"><span data-stu-id="dd754-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="dd754-110">A második parancs frissíti a címkét, a harmadik pedig hozzáadja a hálózati felület konfigurációját a hálózati profilhoz.</span><span class="sxs-lookup"><span data-stu-id="dd754-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="dd754-111">A negyedik parancs frissíti a hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="dd754-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="dd754-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd754-112">PARAMETERS</span></span>

### <span data-ttu-id="dd754-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd754-113">-AsJob</span></span>
<span data-ttu-id="dd754-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dd754-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd754-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd754-115">-DefaultProfile</span></span>
<span data-ttu-id="dd754-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd754-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd754-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd754-117">-NetworkProfile</span></span>
<span data-ttu-id="dd754-118">A hálózati profil</span><span class="sxs-lookup"><span data-stu-id="dd754-118">The network profile</span></span>

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

### <span data-ttu-id="dd754-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd754-119">-Confirm</span></span>
<span data-ttu-id="dd754-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dd754-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd754-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd754-121">-WhatIf</span></span>
<span data-ttu-id="dd754-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dd754-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd754-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd754-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd754-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd754-124">CommonParameters</span></span>
<span data-ttu-id="dd754-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd754-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd754-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd754-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd754-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd754-127">INPUTS</span></span>

### <span data-ttu-id="dd754-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd754-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="dd754-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd754-129">OUTPUTS</span></span>

### <span data-ttu-id="dd754-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd754-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="dd754-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd754-131">NOTES</span></span>

## <span data-ttu-id="dd754-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd754-132">RELATED LINKS</span></span>

[<span data-ttu-id="dd754-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd754-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="dd754-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd754-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="dd754-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd754-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
