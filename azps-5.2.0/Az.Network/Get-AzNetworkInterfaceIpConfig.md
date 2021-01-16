---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341669"
---
# <span data-ttu-id="0b4cd-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b4cd-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="0b4cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4cd-103">Hálózati felület IP-konfigurációját használja a hálózati felülethez.</span><span class="sxs-lookup"><span data-stu-id="0b4cd-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="0b4cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b4cd-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b4cd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b4cd-105">DESCRIPTION</span></span>
<span data-ttu-id="0b4cd-106">A **Get-AzNetworkInterfaceIPConfig** parancsmag egy Hálózati felület IP-konfigurációt kap egy Azure hálózati felületről.</span><span class="sxs-lookup"><span data-stu-id="0b4cd-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="0b4cd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b4cd-107">EXAMPLES</span></span>

### <span data-ttu-id="0b4cd-108">1: Hálózati felület IP-konfigurációjának beállítása</span><span class="sxs-lookup"><span data-stu-id="0b4cd-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="0b4cd-109">Az első parancs egy mynic nevű meglévő hálózati felületet kap, és a $nic 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0b4cd-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="0b4cd-110">A második parancs a hálózati felület ipconfig1 ipconfig1 nevű IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0b4cd-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="0b4cd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b4cd-111">PARAMETERS</span></span>

### <span data-ttu-id="0b4cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4cd-112">-DefaultProfile</span></span>
<span data-ttu-id="0b4cd-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b4cd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b4cd-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0b4cd-114">-Name</span></span>
<span data-ttu-id="0b4cd-115">A parancsmag hálózati IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b4cd-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0b4cd-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0b4cd-116">-NetworkInterface</span></span>
<span data-ttu-id="0b4cd-117">Egy **NetworkInterface objektumot** ad meg, amely a parancsmag hálózati IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0b4cd-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0b4cd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4cd-118">CommonParameters</span></span>
<span data-ttu-id="0b4cd-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4cd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4cd-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b4cd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4cd-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b4cd-121">INPUTS</span></span>

### <span data-ttu-id="0b4cd-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0b4cd-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="0b4cd-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b4cd-123">OUTPUTS</span></span>

### <span data-ttu-id="0b4cd-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4cd-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="0b4cd-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b4cd-125">NOTES</span></span>
* <span data-ttu-id="0b4cd-126">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="0b4cd-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0b4cd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b4cd-127">RELATED LINKS</span></span>

[<span data-ttu-id="0b4cd-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b4cd-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0b4cd-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b4cd-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0b4cd-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b4cd-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0b4cd-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b4cd-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


