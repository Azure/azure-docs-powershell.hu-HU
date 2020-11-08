---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186206"
---
# <span data-ttu-id="f68c9-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f68c9-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="f68c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f68c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f68c9-103">A virtuális hálózati átjárón a virtuális hálózati átjárón beállított VPN IPSec-paramétereket a webhely kapcsolatai pontra irányítja.</span><span class="sxs-lookup"><span data-stu-id="f68c9-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="f68c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f68c9-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f68c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f68c9-105">DESCRIPTION</span></span>
<span data-ttu-id="f68c9-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f68c9-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f68c9-107">A **Get-AzVpnClientIpsecParameter** parancsmag az Azure-beli átjárón alapuló IPSec-paramétereket az átjáró neve és az erőforrás csoport neve alapján adja meg.</span><span class="sxs-lookup"><span data-stu-id="f68c9-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="f68c9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f68c9-108">EXAMPLES</span></span>

### <span data-ttu-id="f68c9-109">1. példa: a virtuális hálózati átjárón beállított VPN IPSec-paraméterek bekapcsolása a webhely kapcsolatai pontra.</span><span class="sxs-lookup"><span data-stu-id="f68c9-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="f68c9-110">A virtuális hálózati átjárón beállított VPN IPSec-paraméterek objektumát adja eredményül a "myGateway" nevű erőforráscsoport "myRG" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="f68c9-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="f68c9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f68c9-111">PARAMETERS</span></span>

### <span data-ttu-id="f68c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f68c9-112">-DefaultProfile</span></span>
<span data-ttu-id="f68c9-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f68c9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f68c9-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f68c9-114">-Name</span></span>
<span data-ttu-id="f68c9-115">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f68c9-115">The resource name.</span></span>

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

### <span data-ttu-id="f68c9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f68c9-116">-ResourceGroupName</span></span>
<span data-ttu-id="f68c9-117">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f68c9-117">The resource group name.</span></span>

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

### <span data-ttu-id="f68c9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68c9-118">CommonParameters</span></span>
<span data-ttu-id="f68c9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f68c9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68c9-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f68c9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68c9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f68c9-121">INPUTS</span></span>

### <span data-ttu-id="f68c9-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f68c9-122">System.String</span></span>

## <span data-ttu-id="f68c9-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f68c9-123">OUTPUTS</span></span>

### <span data-ttu-id="f68c9-124">Microsoft. Azure. commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="f68c9-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="f68c9-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f68c9-125">NOTES</span></span>

## <span data-ttu-id="f68c9-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f68c9-126">RELATED LINKS</span></span>

[<span data-ttu-id="f68c9-127">Új – AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f68c9-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="f68c9-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f68c9-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="f68c9-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="f68c9-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)