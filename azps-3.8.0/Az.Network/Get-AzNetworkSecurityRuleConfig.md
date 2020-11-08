---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3d8b2445d6bb1c92d7246f1d9f33a06dfef3c58b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013315"
---
# <span data-ttu-id="fa315-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa315-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="fa315-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa315-102">SYNOPSIS</span></span>
<span data-ttu-id="fa315-103">Hálózatbiztonsági szabály beállítása hálózati biztonsági csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="fa315-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="fa315-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa315-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa315-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa315-105">DESCRIPTION</span></span>
<span data-ttu-id="fa315-106">A **Get-AzNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabály konfigurációt kap az Azure-hálózat biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="fa315-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="fa315-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fa315-107">EXAMPLES</span></span>

### <span data-ttu-id="fa315-108">1: hálózati biztonsági szabály konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="fa315-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="fa315-109">Ez a parancs beolvassa az "AllowInternetOutBound" nevű "nsg1" nevű Azure Network biztonsági csoport "rg1" nevű "" nevű alapértelmezett szabályát.</span><span class="sxs-lookup"><span data-stu-id="fa315-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="fa315-110">2: a hálózati biztonsági szabály konfigurációjának beolvasása csak a név használatával</span><span class="sxs-lookup"><span data-stu-id="fa315-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="fa315-111">Ez a parancs a "rg1" erőforráscsoport "nsg1" erőforráscsoport nevű Azure Network biztonsági csoportjának "RDP-szabály" nevű, felhasználó által definiált szabályát olvassa be</span><span class="sxs-lookup"><span data-stu-id="fa315-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="fa315-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa315-112">PARAMETERS</span></span>

### <span data-ttu-id="fa315-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa315-113">-DefaultProfile</span></span>
<span data-ttu-id="fa315-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa315-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa315-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="fa315-115">-DefaultRules</span></span>
<span data-ttu-id="fa315-116">Azt jelzi, hogy a parancsmag a felhasználó által létrehozott szabály-konfigurációt vagy alapértelmezett szabály-konfigurációt kap-e.</span><span class="sxs-lookup"><span data-stu-id="fa315-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="fa315-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa315-117">-Name</span></span>
<span data-ttu-id="fa315-118">A beolvasás hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa315-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="fa315-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fa315-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fa315-120">Itt adhatja meg azt a **NetworkSecurityGroup** -objektumot, amely a beolvasás hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fa315-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="fa315-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa315-121">CommonParameters</span></span>
<span data-ttu-id="fa315-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa315-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa315-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa315-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa315-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa315-124">INPUTS</span></span>

### <span data-ttu-id="fa315-125">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fa315-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="fa315-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa315-126">OUTPUTS</span></span>

### <span data-ttu-id="fa315-127">Microsoft. Azure. commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="fa315-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="fa315-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa315-128">NOTES</span></span>

## <span data-ttu-id="fa315-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa315-129">RELATED LINKS</span></span>

[<span data-ttu-id="fa315-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa315-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fa315-131">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa315-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fa315-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa315-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fa315-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fa315-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


