---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372566"
---
# <span data-ttu-id="19adf-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="19adf-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="19adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19adf-102">SYNOPSIS</span></span>
<span data-ttu-id="19adf-103">Lehetővé teszi a felhasználóknak, hogy egyszerűen letöltsék a virtuális magánhálózati parancsmaggal létrehozott Vpn-New-AzVpnClientConfiguration csomagot.</span><span class="sxs-lookup"><span data-stu-id="19adf-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="19adf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19adf-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19adf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19adf-105">DESCRIPTION</span></span>
<span data-ttu-id="19adf-106">A Get-AzVpnClientConfiguration adja vissza azt az URL-címet, ahonnan a VPN-ügyfél letölthető.</span><span class="sxs-lookup"><span data-stu-id="19adf-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="19adf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19adf-107">EXAMPLES</span></span>

### <span data-ttu-id="19adf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="19adf-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="19adf-109">A korábban a windowsos parancs használatával létrehozott VpnClient-profil letöltésére New-AzVpnClientConfiguration URL-címet.</span><span class="sxs-lookup"><span data-stu-id="19adf-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="19adf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19adf-110">PARAMETERS</span></span>

### <span data-ttu-id="19adf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19adf-111">-DefaultProfile</span></span>
<span data-ttu-id="19adf-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19adf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19adf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="19adf-113">-Name</span></span>
<span data-ttu-id="19adf-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="19adf-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19adf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19adf-115">-ResourceGroupName</span></span>
<span data-ttu-id="19adf-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="19adf-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19adf-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19adf-117">-Confirm</span></span>
<span data-ttu-id="19adf-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="19adf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19adf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19adf-119">-WhatIf</span></span>
<span data-ttu-id="19adf-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="19adf-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19adf-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19adf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19adf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19adf-122">CommonParameters</span></span>
<span data-ttu-id="19adf-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19adf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19adf-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19adf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19adf-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19adf-125">INPUTS</span></span>

### <span data-ttu-id="19adf-126">System.String</span><span class="sxs-lookup"><span data-stu-id="19adf-126">System.String</span></span>

## <span data-ttu-id="19adf-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19adf-127">OUTPUTS</span></span>

### <span data-ttu-id="19adf-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="19adf-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="19adf-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19adf-129">NOTES</span></span>

## <span data-ttu-id="19adf-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19adf-130">RELATED LINKS</span></span>

[<span data-ttu-id="19adf-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="19adf-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
