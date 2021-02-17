---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156970"
---
# <span data-ttu-id="551ab-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="551ab-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="551ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="551ab-102">SYNOPSIS</span></span>
<span data-ttu-id="551ab-103">Hálózati felület IP-konfigurációját használja a hálózati felülethez.</span><span class="sxs-lookup"><span data-stu-id="551ab-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="551ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="551ab-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="551ab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="551ab-105">DESCRIPTION</span></span>
<span data-ttu-id="551ab-106">A **Get-AzNetworkInterfaceIPConfig** parancsmag egy hálózati felület IP-konfigurációját kapja egy Azure hálózati felületről.</span><span class="sxs-lookup"><span data-stu-id="551ab-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="551ab-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="551ab-107">EXAMPLES</span></span>

### <span data-ttu-id="551ab-108">1: Hálózati felület IP-konfigurációjának beállítása</span><span class="sxs-lookup"><span data-stu-id="551ab-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="551ab-109">Az első parancs egy mynic nevű meglévő hálózati felületet kap, és a $nic 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="551ab-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="551ab-110">A második parancs a hálózati felület ipconfig1 ipconfig1 nevű IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="551ab-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="551ab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="551ab-111">PARAMETERS</span></span>

### <span data-ttu-id="551ab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551ab-112">-DefaultProfile</span></span>
<span data-ttu-id="551ab-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="551ab-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="551ab-114">-Name</span><span class="sxs-lookup"><span data-stu-id="551ab-114">-Name</span></span>
<span data-ttu-id="551ab-115">A parancsmag hálózati IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="551ab-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551ab-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="551ab-116">-NetworkInterface</span></span>
<span data-ttu-id="551ab-117">Egy **NetworkInterface objektumot** ad meg, amely a parancsmag hálózati IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="551ab-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="551ab-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551ab-118">CommonParameters</span></span>
<span data-ttu-id="551ab-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551ab-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551ab-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="551ab-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551ab-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="551ab-121">INPUTS</span></span>

### <span data-ttu-id="551ab-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="551ab-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="551ab-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="551ab-123">OUTPUTS</span></span>

### <span data-ttu-id="551ab-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="551ab-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="551ab-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="551ab-125">NOTES</span></span>
* <span data-ttu-id="551ab-126">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="551ab-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="551ab-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="551ab-127">RELATED LINKS</span></span>

[<span data-ttu-id="551ab-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="551ab-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="551ab-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="551ab-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="551ab-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="551ab-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="551ab-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="551ab-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


