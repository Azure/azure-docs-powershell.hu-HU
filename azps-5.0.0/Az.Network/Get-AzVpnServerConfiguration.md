---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188123"
---
# <span data-ttu-id="c7d85-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d85-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="c7d85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7d85-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d85-103">Meglévő VpnServerConfiguration kap a webhelyhez való kapcsolódáshoz.</span><span class="sxs-lookup"><span data-stu-id="c7d85-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="c7d85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7d85-104">SYNTAX</span></span>

### <span data-ttu-id="c7d85-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7d85-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d85-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d85-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d85-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7d85-107">DESCRIPTION</span></span>
<span data-ttu-id="c7d85-108">A **Get-AzVpnServerConfiguration** parancsmag a meglévő VpnServerConfiguration jeleníti meg a webhely kapcsolódási pontjára.</span><span class="sxs-lookup"><span data-stu-id="c7d85-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="c7d85-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c7d85-109">EXAMPLES</span></span>

### <span data-ttu-id="c7d85-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c7d85-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="c7d85-111">A fenti parancs a meglévő VpnServerConfiguration fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="c7d85-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="c7d85-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7d85-112">PARAMETERS</span></span>

### <span data-ttu-id="c7d85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d85-113">-DefaultProfile</span></span>
<span data-ttu-id="c7d85-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7d85-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7d85-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7d85-115">-Name</span></span>
<span data-ttu-id="c7d85-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c7d85-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d85-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d85-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7d85-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7d85-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d85-119">CommonParameters</span></span>
<span data-ttu-id="c7d85-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7d85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d85-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d85-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d85-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7d85-122">INPUTS</span></span>

### <span data-ttu-id="c7d85-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c7d85-123">None</span></span>

## <span data-ttu-id="c7d85-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7d85-124">OUTPUTS</span></span>

### <span data-ttu-id="c7d85-125">Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d85-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="c7d85-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7d85-126">NOTES</span></span>

## <span data-ttu-id="c7d85-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7d85-127">RELATED LINKS</span></span>
