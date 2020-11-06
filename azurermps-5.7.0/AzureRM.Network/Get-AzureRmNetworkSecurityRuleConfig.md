---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 1f31e26c677777867f92e9e0a0e35bfa26eb4e5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505464"
---
# <span data-ttu-id="e8ce4-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8ce4-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="e8ce4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ce4-103">Hálózatbiztonsági szabály beállítása hálózati biztonsági csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8ce4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8ce4-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ce4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ce4-106">A **Get-AzureRmNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabály konfigurációt kap az Azure-hálózat biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="e8ce4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e8ce4-107">EXAMPLES</span></span>

### <span data-ttu-id="e8ce4-108">1: hálózati biztonsági szabály konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="e8ce4-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="e8ce4-109">Ez a parancs beolvassa az "AllowInternetOutBound" nevű "nsg1" nevű Azure Network biztonsági csoport "rg1" nevű "" nevű alapértelmezett szabályát.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="e8ce4-110">2: a hálózati biztonsági szabály konfigurációjának beolvasása csak a név használatával</span><span class="sxs-lookup"><span data-stu-id="e8ce4-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="e8ce4-111">Ez a parancs a "rg1" erőforráscsoport "nsg1" erőforráscsoport nevű Azure Network biztonsági csoportjának "RDP-szabály" nevű, felhasználó által definiált szabályát olvassa be</span><span class="sxs-lookup"><span data-stu-id="e8ce4-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="e8ce4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8ce4-112">PARAMETERS</span></span>

### <span data-ttu-id="e8ce4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ce4-113">-DefaultProfile</span></span>
<span data-ttu-id="e8ce4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8ce4-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="e8ce4-115">-DefaultRules</span></span>
<span data-ttu-id="e8ce4-116">Azt jelzi, hogy a parancsmag a felhasználó által létrehozott szabály-konfigurációt vagy alapértelmezett szabály-konfigurációt kap-e.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="e8ce4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8ce4-117">-Name</span></span>
<span data-ttu-id="e8ce4-118">A beolvasás hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="e8ce4-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8ce4-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e8ce4-120">Itt adhatja meg azt a **NetworkSecurityGroup** -objektumot, amely a beolvasás hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e8ce4-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="e8ce4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ce4-121">CommonParameters</span></span>
<span data-ttu-id="e8ce4-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8ce4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ce4-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ce4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ce4-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ce4-124">INPUTS</span></span>

### <span data-ttu-id="e8ce4-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8ce4-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="e8ce4-126">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e8ce4-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="e8ce4-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ce4-127">OUTPUTS</span></span>

### <span data-ttu-id="e8ce4-128">Microsoft. Azure. commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="e8ce4-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="e8ce4-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8ce4-129">NOTES</span></span>

## <span data-ttu-id="e8ce4-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8ce4-130">RELATED LINKS</span></span>

[<span data-ttu-id="e8ce4-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8ce4-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e8ce4-132">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8ce4-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e8ce4-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8ce4-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e8ce4-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8ce4-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


