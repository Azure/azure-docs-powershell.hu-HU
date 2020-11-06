---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 9ab4af1eefa6214d43eca84f65053eeecb12d912
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495068"
---
# <span data-ttu-id="e3bd0-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3bd0-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="e3bd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bd0-103">Lehetővé teszi a felhasználóknak, hogy egyszerűen töltse le a New-AzureRmVpnClientConfiguration parancsmagot létrehozott VPN-profil csomagot.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3bd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3bd0-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3bd0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="e3bd0-106">A Get-AzureRmVpnClientConfiguration azt az URL-címet jeleníti meg, amelyben a VPN-ügyfél letölthető.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-106">The Get-AzureRmVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="e3bd0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e3bd0-107">EXAMPLES</span></span>

### <span data-ttu-id="e3bd0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3bd0-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="e3bd0-109">Az URL-cím megadásával letöltheti azt a VpnClient-profilt, amelyet korábban a New-AzureRMVpnClientConfiguration parancs segítségével generált.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="e3bd0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3bd0-110">PARAMETERS</span></span>

### <span data-ttu-id="e3bd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bd0-111">-DefaultProfile</span></span>
<span data-ttu-id="e3bd0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3bd0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3bd0-113">-Name</span></span>
<span data-ttu-id="e3bd0-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-114">The resource name.</span></span>

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

### <span data-ttu-id="e3bd0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3bd0-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3bd0-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-116">The resource group name.</span></span>

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

### <span data-ttu-id="e3bd0-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3bd0-117">-Confirm</span></span>
<span data-ttu-id="e3bd0-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3bd0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bd0-119">-WhatIf</span></span>
<span data-ttu-id="e3bd0-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3bd0-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3bd0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3bd0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bd0-122">CommonParameters</span></span>
<span data-ttu-id="e3bd0-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3bd0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bd0-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3bd0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bd0-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3bd0-125">INPUTS</span></span>

### <span data-ttu-id="e3bd0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e3bd0-126">System.String</span></span>

## <span data-ttu-id="e3bd0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3bd0-127">OUTPUTS</span></span>

### <span data-ttu-id="e3bd0-128">Microsoft. Azure. commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="e3bd0-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="e3bd0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3bd0-129">NOTES</span></span>

## <span data-ttu-id="e3bd0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3bd0-130">RELATED LINKS</span></span>
