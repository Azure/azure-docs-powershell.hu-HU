---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379748"
---
# <span data-ttu-id="9f96c-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f96c-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="9f96c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f96c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f96c-103">Beállítja az ezzel a VirtualWannal társított Összes VpnServerConfiguráció listáját.</span><span class="sxs-lookup"><span data-stu-id="9f96c-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="9f96c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f96c-104">SYNTAX</span></span>

### <span data-ttu-id="9f96c-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f96c-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f96c-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9f96c-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f96c-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9f96c-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f96c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f96c-108">DESCRIPTION</span></span>
<span data-ttu-id="9f96c-109">A **Get-AzVirtualWanVpnServerConfiguration** parancsmag visszaadja a VirtualWannal társított összes VpnServerConfigurations listáját.</span><span class="sxs-lookup"><span data-stu-id="9f96c-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="9f96c-110">i.e. Minden VpnServerConfigurations, amely a VirtualWan VirutalHubs rendszerében lévő P2SVpnGatewayshez van csatolva.</span><span class="sxs-lookup"><span data-stu-id="9f96c-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="9f96c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f96c-111">EXAMPLES</span></span>

### <span data-ttu-id="9f96c-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9f96c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="9f96c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f96c-113">PARAMETERS</span></span>

### <span data-ttu-id="9f96c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f96c-114">-DefaultProfile</span></span>
<span data-ttu-id="9f96c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f96c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f96c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9f96c-116">-Name</span></span>
<span data-ttu-id="9f96c-117">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9f96c-117">The resource name.</span></span>

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

### <span data-ttu-id="9f96c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f96c-118">-ResourceGroupName</span></span>
<span data-ttu-id="9f96c-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9f96c-119">The resource group name.</span></span>

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

### <span data-ttu-id="9f96c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f96c-120">-ResourceId</span></span>
<span data-ttu-id="9f96c-121">A virtuális wan Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="9f96c-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f96c-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9f96c-122">-VirtualWanObject</span></span>
<span data-ttu-id="9f96c-123">A virtuális wan objektum.</span><span class="sxs-lookup"><span data-stu-id="9f96c-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f96c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f96c-124">CommonParameters</span></span>
<span data-ttu-id="9f96c-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f96c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f96c-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f96c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f96c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f96c-127">INPUTS</span></span>

### <span data-ttu-id="9f96c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9f96c-128">System.String</span></span>
<span data-ttu-id="9f96c-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9f96c-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="9f96c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f96c-130">OUTPUTS</span></span>

### <span data-ttu-id="9f96c-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="9f96c-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="9f96c-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f96c-132">NOTES</span></span>

## <span data-ttu-id="9f96c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f96c-133">RELATED LINKS</span></span>
