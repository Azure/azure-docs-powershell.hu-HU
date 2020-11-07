---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 184e1291f134b52ee57a239327bb45da4a4481ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841597"
---
# <span data-ttu-id="a8940-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8940-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="a8940-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8940-102">SYNOPSIS</span></span>
<span data-ttu-id="a8940-103">Hálózatbiztonsági szabály beállítása hálózati biztonsági csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="a8940-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="a8940-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8940-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8940-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8940-105">DESCRIPTION</span></span>
<span data-ttu-id="a8940-106">A **Get-AzNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabály konfigurációt kap az Azure-hálózat biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="a8940-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="a8940-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8940-107">EXAMPLES</span></span>

### <span data-ttu-id="a8940-108">1: hálózati biztonsági szabály konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a8940-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="a8940-109">Ez a parancs beolvassa az "AllowInternetOutBound" nevű "nsg1" nevű Azure Network biztonsági csoport "rg1" nevű "" nevű alapértelmezett szabályát.</span><span class="sxs-lookup"><span data-stu-id="a8940-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="a8940-110">2: a hálózati biztonsági szabály konfigurációjának beolvasása csak a név használatával</span><span class="sxs-lookup"><span data-stu-id="a8940-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="a8940-111">Ez a parancs a "rg1" erőforráscsoport "nsg1" erőforráscsoport nevű Azure Network biztonsági csoportjának "RDP-szabály" nevű, felhasználó által definiált szabályát olvassa be</span><span class="sxs-lookup"><span data-stu-id="a8940-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="a8940-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8940-112">PARAMETERS</span></span>

### <span data-ttu-id="a8940-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8940-113">-DefaultProfile</span></span>
<span data-ttu-id="a8940-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8940-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8940-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="a8940-115">-DefaultRules</span></span>
<span data-ttu-id="a8940-116">Azt jelzi, hogy a parancsmag a felhasználó által létrehozott szabály-konfigurációt vagy alapértelmezett szabály-konfigurációt kap-e.</span><span class="sxs-lookup"><span data-stu-id="a8940-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="a8940-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8940-117">-Name</span></span>
<span data-ttu-id="a8940-118">A beolvasás hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8940-118">Specifies the name of the network security rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8940-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8940-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a8940-120">Itt adhatja meg azt a **NetworkSecurityGroup** -objektumot, amely a beolvasás hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a8940-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="a8940-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8940-121">CommonParameters</span></span>
<span data-ttu-id="a8940-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8940-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8940-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8940-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8940-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8940-124">INPUTS</span></span>

### <span data-ttu-id="a8940-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8940-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="a8940-126">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a8940-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="a8940-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8940-127">OUTPUTS</span></span>

### <span data-ttu-id="a8940-128">Microsoft. Azure. commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="a8940-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="a8940-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8940-129">NOTES</span></span>

## <span data-ttu-id="a8940-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8940-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8940-131">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8940-131">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a8940-132">Új – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8940-132">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a8940-133">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8940-133">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a8940-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8940-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


