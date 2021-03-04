---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3be81626dc48f66fd7aac71c23c2cd9168dab336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006262"
---
# <span data-ttu-id="d3140-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d3140-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="d3140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3140-102">SYNOPSIS</span></span>
<span data-ttu-id="d3140-103">A virtuális hálózati átjáró virtuális hálózati átjárójára vonatkozó IPsec-paramétereket adja meg a point to site connections beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="d3140-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="d3140-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3140-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3140-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3140-105">DESCRIPTION</span></span>
<span data-ttu-id="d3140-106">A virtuális hálózati átjáró az azure-beli átjárót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="d3140-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d3140-107">A **Get-AzVpnClientIpsecParameter** parancsmag az Átjáró neve és az Erőforráscsoport neve alapján visszaadja az Azure-átjárón beállított vpn ipsec-paraméterek objektumát.</span><span class="sxs-lookup"><span data-stu-id="d3140-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="d3140-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3140-108">EXAMPLES</span></span>

### <span data-ttu-id="d3140-109">1. példa: A virtuális hálózati átjáró virtuális hálózati átjárón megadott IPsec-paramétereit adja meg a Point to site connections beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="d3140-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="d3140-110">A virtuális hálózati átjárón a "myGateway" nevű vpn ipsec-paraméterek objektumát adja eredményül a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="d3140-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="d3140-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3140-111">PARAMETERS</span></span>

### <span data-ttu-id="d3140-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3140-112">-DefaultProfile</span></span>
<span data-ttu-id="d3140-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3140-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3140-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d3140-114">-Name</span></span>
<span data-ttu-id="d3140-115">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d3140-115">The resource name.</span></span>

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

### <span data-ttu-id="d3140-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3140-116">-ResourceGroupName</span></span>
<span data-ttu-id="d3140-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3140-117">The resource group name.</span></span>

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

### <span data-ttu-id="d3140-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3140-118">CommonParameters</span></span>
<span data-ttu-id="d3140-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3140-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3140-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3140-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3140-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3140-121">INPUTS</span></span>

### <span data-ttu-id="d3140-122">System.String</span><span class="sxs-lookup"><span data-stu-id="d3140-122">System.String</span></span>

## <span data-ttu-id="d3140-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3140-123">OUTPUTS</span></span>

### <span data-ttu-id="d3140-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d3140-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="d3140-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3140-125">NOTES</span></span>

## <span data-ttu-id="d3140-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3140-126">RELATED LINKS</span></span>

[<span data-ttu-id="d3140-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d3140-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="d3140-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d3140-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="d3140-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d3140-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
