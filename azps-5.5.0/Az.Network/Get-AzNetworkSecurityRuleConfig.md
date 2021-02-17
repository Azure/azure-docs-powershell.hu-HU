---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3d8b2445d6bb1c92d7246f1d9f33a06dfef3c58b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206942"
---
# <span data-ttu-id="cab62-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cab62-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="cab62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab62-102">SYNOPSIS</span></span>
<span data-ttu-id="cab62-103">Hálózati biztonsági szabály beállítása hálózati biztonsági csoportokhoz</span><span class="sxs-lookup"><span data-stu-id="cab62-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="cab62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cab62-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cab62-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cab62-105">DESCRIPTION</span></span>
<span data-ttu-id="cab62-106">A **Get-AzNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabálykonfigurációt kap egy Azure-hálózat biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="cab62-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="cab62-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cab62-107">EXAMPLES</span></span>

### <span data-ttu-id="cab62-108">1: Hálózati biztonsági szabály konfidigének beolvasása</span><span class="sxs-lookup"><span data-stu-id="cab62-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="cab62-109">Ez a parancs beolvassa az "AllowInternetOutBound" nevű alapértelmezett szabályt az "rg1" erőforráscsoportban az "nsg1" nevű Azure hálózati biztonsági csoportból.</span><span class="sxs-lookup"><span data-stu-id="cab62-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="cab62-110">2: Hálózati biztonsági szabály konfidigének beolvasása csak a név használatával</span><span class="sxs-lookup"><span data-stu-id="cab62-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="cab62-111">Ez a parancs lekéri az "rdp-rule" nevű felhasználó által definiált szabályt az "rg1" erőforráscsoportban az "nsg1" nevű Azure hálózati biztonsági csoportból.</span><span class="sxs-lookup"><span data-stu-id="cab62-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="cab62-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cab62-112">PARAMETERS</span></span>

### <span data-ttu-id="cab62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab62-113">-DefaultProfile</span></span>
<span data-ttu-id="cab62-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cab62-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cab62-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="cab62-115">-DefaultRules</span></span>
<span data-ttu-id="cab62-116">Azt jelzi, hogy ez a parancsmag felhasználó által létrehozott vagy alapértelmezett szabálykonfigurációt kap-e.</span><span class="sxs-lookup"><span data-stu-id="cab62-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="cab62-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cab62-117">-Name</span></span>
<span data-ttu-id="cab62-118">A lekért hálózati biztonsági szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cab62-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="cab62-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cab62-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cab62-120">Egy **NetworkSecurityGroup-objektumot** ad meg, amely tartalmazza a behozni kívánt hálózati biztonsági szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="cab62-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="cab62-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab62-121">CommonParameters</span></span>
<span data-ttu-id="cab62-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab62-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab62-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cab62-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab62-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cab62-124">INPUTS</span></span>

### <span data-ttu-id="cab62-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cab62-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="cab62-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab62-126">OUTPUTS</span></span>

### <span data-ttu-id="cab62-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="cab62-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="cab62-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cab62-128">NOTES</span></span>

## <span data-ttu-id="cab62-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cab62-129">RELATED LINKS</span></span>

[<span data-ttu-id="cab62-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cab62-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cab62-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cab62-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cab62-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cab62-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cab62-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cab62-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


