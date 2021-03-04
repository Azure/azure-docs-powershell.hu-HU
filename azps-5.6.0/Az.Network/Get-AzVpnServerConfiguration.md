---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 0d669aca3eaf330322ff814f51bd0c412400f457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925458"
---
# <span data-ttu-id="8e145-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e145-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="8e145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e145-102">SYNOPSIS</span></span>
<span data-ttu-id="8e145-103">Egy meglévő VpnServerConfigurationt kap, amely a webhelyre mutat.</span><span class="sxs-lookup"><span data-stu-id="8e145-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="8e145-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e145-104">SYNTAX</span></span>

### <span data-ttu-id="8e145-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e145-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e145-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e145-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e145-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e145-107">DESCRIPTION</span></span>
<span data-ttu-id="8e145-108">A **Get-AzVpnServerConfiguration** parancsmag a Point to site connectivity meglévő VpnServerConfiguration parancsmagját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8e145-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="8e145-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e145-109">EXAMPLES</span></span>

### <span data-ttu-id="8e145-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e145-110">Example 1</span></span>
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

<span data-ttu-id="8e145-111">A fenti parancs a meglévő VpnServerConfigurationt fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="8e145-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="8e145-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e145-112">PARAMETERS</span></span>

### <span data-ttu-id="8e145-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e145-113">-DefaultProfile</span></span>
<span data-ttu-id="8e145-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e145-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e145-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8e145-115">-Name</span></span>
<span data-ttu-id="8e145-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8e145-116">The resource name.</span></span>

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

### <span data-ttu-id="8e145-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e145-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e145-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8e145-118">The resource group name.</span></span>

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

### <span data-ttu-id="8e145-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e145-119">CommonParameters</span></span>
<span data-ttu-id="8e145-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e145-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e145-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e145-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e145-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e145-122">INPUTS</span></span>

### <span data-ttu-id="8e145-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e145-123">None</span></span>

## <span data-ttu-id="8e145-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e145-124">OUTPUTS</span></span>

### <span data-ttu-id="8e145-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e145-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="8e145-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e145-126">NOTES</span></span>

## <span data-ttu-id="8e145-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e145-127">RELATED LINKS</span></span>
