---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151795"
---
# <span data-ttu-id="b0762-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0762-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="b0762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0762-102">SYNOPSIS</span></span>
<span data-ttu-id="b0762-103">Egy meglévő VpnServerConfigurációt kap a webhelyre való kapcsolódáshoz.</span><span class="sxs-lookup"><span data-stu-id="b0762-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="b0762-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0762-104">SYNTAX</span></span>

### <span data-ttu-id="b0762-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0762-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0762-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0762-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0762-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0762-107">DESCRIPTION</span></span>
<span data-ttu-id="b0762-108">A **Get-AzVpnServerConfiguration** parancsmag a Point to site connectivity meglévő VpnServerConfiguration parancsmagját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b0762-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="b0762-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0762-109">EXAMPLES</span></span>

### <span data-ttu-id="b0762-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b0762-110">Example 1</span></span>
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

<span data-ttu-id="b0762-111">A fenti parancs a meglévő VpnServerConfigurationt fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="b0762-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="b0762-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0762-112">PARAMETERS</span></span>

### <span data-ttu-id="b0762-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0762-113">-DefaultProfile</span></span>
<span data-ttu-id="b0762-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0762-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0762-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b0762-115">-Name</span></span>
<span data-ttu-id="b0762-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b0762-116">The resource name.</span></span>

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

### <span data-ttu-id="b0762-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0762-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0762-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b0762-118">The resource group name.</span></span>

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

### <span data-ttu-id="b0762-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0762-119">CommonParameters</span></span>
<span data-ttu-id="b0762-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0762-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0762-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0762-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0762-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0762-122">INPUTS</span></span>

### <span data-ttu-id="b0762-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b0762-123">None</span></span>

## <span data-ttu-id="b0762-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0762-124">OUTPUTS</span></span>

### <span data-ttu-id="b0762-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0762-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b0762-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0762-126">NOTES</span></span>

## <span data-ttu-id="b0762-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0762-127">RELATED LINKS</span></span>
