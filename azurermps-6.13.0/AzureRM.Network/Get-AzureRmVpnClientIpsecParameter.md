---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495067"
---
# <span data-ttu-id="5a30b-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="5a30b-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="5a30b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a30b-102">SYNOPSIS</span></span>
<span data-ttu-id="5a30b-103">A virtuális hálózati átjárón a virtuális hálózati átjárón beállított VPN IPSec-paramétereket a webhely kapcsolatai pontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="5a30b-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a30b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a30b-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a30b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a30b-105">DESCRIPTION</span></span>
<span data-ttu-id="5a30b-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5a30b-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="5a30b-107">A **Get-AzureRmVpnClientIpsecParameter** parancsmag az Azure-beli átjárón alapuló IPSec-paramétereket az átjáró neve és az erőforrás csoport neve alapján adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a30b-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="5a30b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5a30b-108">EXAMPLES</span></span>

### <span data-ttu-id="5a30b-109">1: a virtuális hálózati átjárón beállított VPN IPSec-paraméterek bekapcsolása a webhely kapcsolatai pontra.</span><span class="sxs-lookup"><span data-stu-id="5a30b-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="5a30b-110">A virtuális hálózati átjárón beállított VPN IPSec-paraméterek objektumát adja eredményül a "myGateway" nevű erőforráscsoport "myRG" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5a30b-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="5a30b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a30b-111">PARAMETERS</span></span>

### <span data-ttu-id="5a30b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a30b-112">-DefaultProfile</span></span>
<span data-ttu-id="5a30b-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a30b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a30b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a30b-114">-Name</span></span>
<span data-ttu-id="5a30b-115">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5a30b-115">The resource name.</span></span>

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

### <span data-ttu-id="5a30b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a30b-116">-ResourceGroupName</span></span>
<span data-ttu-id="5a30b-117">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a30b-117">The resource group name.</span></span>

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

### <span data-ttu-id="5a30b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a30b-118">CommonParameters</span></span>
<span data-ttu-id="5a30b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a30b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a30b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a30b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a30b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a30b-121">INPUTS</span></span>

### <span data-ttu-id="5a30b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5a30b-122">System.String</span></span>

## <span data-ttu-id="5a30b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a30b-123">OUTPUTS</span></span>

### <span data-ttu-id="5a30b-124">Microsoft. Azure. commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="5a30b-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="5a30b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a30b-125">NOTES</span></span>

## <span data-ttu-id="5a30b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a30b-126">RELATED LINKS</span></span>
