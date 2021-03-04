---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: abeeabcc3930a2f18822dbf3d9986e17fbc01c88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940098"
---
# <span data-ttu-id="ebef7-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ebef7-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="ebef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebef7-102">SYNOPSIS</span></span>
<span data-ttu-id="ebef7-103">Eltávolítja a hálózati felületek IP-konfigurációját a hálózati felületekről.</span><span class="sxs-lookup"><span data-stu-id="ebef7-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="ebef7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ebef7-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebef7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ebef7-105">DESCRIPTION</span></span>
<span data-ttu-id="ebef7-106">A **Remove-AzNetworkInterfaceIpConfig** parancsmag eltávolítja a hálózati felületek IP-konfigurációját egy Azure hálózati felületről.</span><span class="sxs-lookup"><span data-stu-id="ebef7-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="ebef7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ebef7-107">EXAMPLES</span></span>

### <span data-ttu-id="ebef7-108">1. példa: IP-konfiguráció törlése hálózati felületről</span><span class="sxs-lookup"><span data-stu-id="ebef7-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="ebef7-109">Az első parancs egy mynic nevű hálózati felületet kap, és azt egy változóban $nic.</span><span class="sxs-lookup"><span data-stu-id="ebef7-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="ebef7-110">A második parancs eltávolítja a hálózati felülettel társított IPConfig-1 IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="ebef7-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="ebef7-111">A harmadik parancs beállítja a hálózati felületen végrehajtott módosításokat.</span><span class="sxs-lookup"><span data-stu-id="ebef7-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="ebef7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebef7-112">PARAMETERS</span></span>

### <span data-ttu-id="ebef7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebef7-113">-DefaultProfile</span></span>
<span data-ttu-id="ebef7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebef7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebef7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ebef7-115">-Name</span></span>
<span data-ttu-id="ebef7-116">Az eltávolítható hálózatifelület-IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebef7-116">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebef7-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ebef7-117">-NetworkInterface</span></span>
<span data-ttu-id="ebef7-118">**NetworkInterface objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="ebef7-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="ebef7-119">Ez az objektum az eltávolítható hálózatifelület-IP-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ebef7-119">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebef7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebef7-120">CommonParameters</span></span>
<span data-ttu-id="ebef7-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebef7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebef7-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebef7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebef7-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebef7-123">INPUTS</span></span>

### <span data-ttu-id="ebef7-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ebef7-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ebef7-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebef7-125">OUTPUTS</span></span>

### <span data-ttu-id="ebef7-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ebef7-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ebef7-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ebef7-127">NOTES</span></span>
* <span data-ttu-id="ebef7-128">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="ebef7-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ebef7-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebef7-129">RELATED LINKS</span></span>

[<span data-ttu-id="ebef7-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ebef7-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ebef7-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ebef7-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ebef7-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ebef7-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ebef7-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ebef7-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


