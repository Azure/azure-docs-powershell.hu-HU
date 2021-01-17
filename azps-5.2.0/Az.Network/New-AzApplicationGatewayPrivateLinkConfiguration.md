---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371684"
---
# <span data-ttu-id="7d69e-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d69e-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="7d69e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d69e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d69e-103">Privát csatolási konfigurációt hoz létre egy alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7d69e-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="7d69e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7d69e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d69e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7d69e-105">DESCRIPTION</span></span>
<span data-ttu-id="7d69e-106">A **New-AzApplicationGatewayPrivateLinkConfiguration** parancsmag létrehoz egy PrivateLink-konfigurációt egy Azure-alkalmazásátjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7d69e-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="7d69e-107">A privát csatolási funkciót csak előlapi IP-konfigurációval lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="7d69e-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="7d69e-108">Egy privát csatolás-konfigurációt legalább egy előlapi IP-konfigurációhoz lehet társítva az alkalmazás-átjárón.</span><span class="sxs-lookup"><span data-stu-id="7d69e-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="7d69e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7d69e-109">EXAMPLES</span></span>

### <span data-ttu-id="7d69e-110">1. példa: Privát hivatkozás konfigurálása egyetlen IP-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="7d69e-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="7d69e-111">Ez a parancs létrehoz egy "privateLinkConfig01" nevű PrivateLink-konfigurációt, és az eredményt a következő nevű változóban $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7d69e-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="7d69e-112">2. példa: Privát hivatkozáskonfiguráció létrehozása több IP-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="7d69e-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="7d69e-113">Ez a parancs létrehoz egy "privateLinkConfig01" nevű PrivateLink-konfigurációt két ipConfigurációval, és az eredményt a $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7d69e-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="7d69e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d69e-114">PARAMETERS</span></span>

### <span data-ttu-id="7d69e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d69e-115">-DefaultProfile</span></span>
<span data-ttu-id="7d69e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d69e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d69e-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d69e-117">-IpConfiguration</span></span>
<span data-ttu-id="7d69e-118">Az ipConfiguration listája</span><span class="sxs-lookup"><span data-stu-id="7d69e-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d69e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7d69e-119">-Name</span></span>
<span data-ttu-id="7d69e-120">A privateLink-konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="7d69e-120">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d69e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d69e-121">-Confirm</span></span>
<span data-ttu-id="7d69e-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7d69e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d69e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d69e-123">-WhatIf</span></span>
<span data-ttu-id="7d69e-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7d69e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d69e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d69e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d69e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d69e-126">CommonParameters</span></span>
<span data-ttu-id="7d69e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d69e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d69e-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d69e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d69e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d69e-129">INPUTS</span></span>

### <span data-ttu-id="7d69e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="7d69e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="7d69e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d69e-131">OUTPUTS</span></span>

### <span data-ttu-id="7d69e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d69e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="7d69e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7d69e-133">NOTES</span></span>

## <span data-ttu-id="7d69e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d69e-134">RELATED LINKS</span></span>

[<span data-ttu-id="7d69e-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d69e-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7d69e-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d69e-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7d69e-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d69e-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7d69e-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d69e-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
