---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 55f2ad108b6392a2f17c7b1539c5ebe7cccc3c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850702"
---
# <span data-ttu-id="9cfe9-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9cfe9-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="9cfe9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cfe9-102">SYNOPSIS</span></span>
<span data-ttu-id="9cfe9-103">Hálózatbiztonsági szabály beállítása hálózati biztonsági csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cfe9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cfe9-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cfe9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cfe9-105">DESCRIPTION</span></span>
<span data-ttu-id="9cfe9-106">A **Get-AzureRmNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabály konfigurációt kap az Azure-hálózat biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="9cfe9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9cfe9-107">EXAMPLES</span></span>

### <span data-ttu-id="9cfe9-108">1: hálózati biztonsági szabály konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="9cfe9-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="9cfe9-109">Ez a parancs beolvassa az "AllowInternetOutBound" nevű "nsg1" nevű Azure Network biztonsági csoport "rg1" nevű "" nevű alapértelmezett szabályát.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="9cfe9-110">2: a hálózati biztonsági szabály konfigurációjának beolvasása csak a név használatával</span><span class="sxs-lookup"><span data-stu-id="9cfe9-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="9cfe9-111">Ez a parancs a "rg1" erőforráscsoport "nsg1" erőforráscsoport nevű Azure Network biztonsági csoportjának "RDP-szabály" nevű, felhasználó által definiált szabályát olvassa be</span><span class="sxs-lookup"><span data-stu-id="9cfe9-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="9cfe9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cfe9-112">PARAMETERS</span></span>

### <span data-ttu-id="9cfe9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cfe9-113">-DefaultProfile</span></span>
<span data-ttu-id="9cfe9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cfe9-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="9cfe9-115">-DefaultRules</span></span>
<span data-ttu-id="9cfe9-116">Azt jelzi, hogy a parancsmag a felhasználó által létrehozott szabály-konfigurációt vagy alapértelmezett szabály-konfigurációt kap-e.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="9cfe9-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9cfe9-117">-Name</span></span>
<span data-ttu-id="9cfe9-118">A beolvasás hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="9cfe9-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9cfe9-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9cfe9-120">Itt adhatja meg azt a **NetworkSecurityGroup** -objektumot, amely a beolvasás hálózati biztonsági szabály konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9cfe9-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="9cfe9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cfe9-121">CommonParameters</span></span>
<span data-ttu-id="9cfe9-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cfe9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cfe9-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cfe9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cfe9-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cfe9-124">INPUTS</span></span>

### <span data-ttu-id="9cfe9-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9cfe9-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="9cfe9-126">A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9cfe9-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="9cfe9-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cfe9-127">OUTPUTS</span></span>

### <span data-ttu-id="9cfe9-128">Microsoft. Azure. commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="9cfe9-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="9cfe9-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cfe9-129">NOTES</span></span>

## <span data-ttu-id="9cfe9-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cfe9-130">RELATED LINKS</span></span>

[<span data-ttu-id="9cfe9-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9cfe9-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9cfe9-132">Új – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9cfe9-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9cfe9-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9cfe9-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9cfe9-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9cfe9-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


