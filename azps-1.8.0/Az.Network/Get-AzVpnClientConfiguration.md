---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: c91b42620d98cae3ecc5dcbd1f8a769c96675ade
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670452"
---
# <span data-ttu-id="06509-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="06509-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="06509-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06509-102">SYNOPSIS</span></span>
<span data-ttu-id="06509-103">Lehetővé teszi a felhasználóknak, hogy egyszerűen töltse le a New-AzVpnClientConfiguration parancsmagot létrehozott VPN-profil csomagot.</span><span class="sxs-lookup"><span data-stu-id="06509-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="06509-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06509-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06509-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06509-105">DESCRIPTION</span></span>
<span data-ttu-id="06509-106">A Get-AzVpnClientConfiguration azt az URL-címet jeleníti meg, amelyben a VPN-ügyfél letölthető.</span><span class="sxs-lookup"><span data-stu-id="06509-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="06509-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06509-107">EXAMPLES</span></span>

### <span data-ttu-id="06509-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06509-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="06509-109">Az URL-cím megadásával letöltheti azt a VpnClient-profilt, amelyet korábban a New-AzVpnClientConfiguration parancs segítségével generált.</span><span class="sxs-lookup"><span data-stu-id="06509-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="06509-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06509-110">PARAMETERS</span></span>

### <span data-ttu-id="06509-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06509-111">-DefaultProfile</span></span>
<span data-ttu-id="06509-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06509-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06509-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06509-113">-Name</span></span>
<span data-ttu-id="06509-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="06509-114">The resource name.</span></span>

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

### <span data-ttu-id="06509-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06509-115">-ResourceGroupName</span></span>
<span data-ttu-id="06509-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="06509-116">The resource group name.</span></span>

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

### <span data-ttu-id="06509-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06509-117">-Confirm</span></span>
<span data-ttu-id="06509-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06509-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06509-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06509-119">-WhatIf</span></span>
<span data-ttu-id="06509-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06509-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06509-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06509-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06509-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06509-122">CommonParameters</span></span>
<span data-ttu-id="06509-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06509-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06509-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="06509-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06509-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06509-125">INPUTS</span></span>

### <span data-ttu-id="06509-126">System. String</span><span class="sxs-lookup"><span data-stu-id="06509-126">System.String</span></span>

## <span data-ttu-id="06509-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06509-127">OUTPUTS</span></span>

### <span data-ttu-id="06509-128">Microsoft. Azure. commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="06509-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="06509-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06509-129">NOTES</span></span>

## <span data-ttu-id="06509-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06509-130">RELATED LINKS</span></span>

[<span data-ttu-id="06509-131">Új – AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="06509-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
