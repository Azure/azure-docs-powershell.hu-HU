---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: de25e096be96e54d2a8aa18f24bf9915a2f16538
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013546"
---
# <span data-ttu-id="428b8-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="428b8-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="428b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="428b8-102">SYNOPSIS</span></span>
<span data-ttu-id="428b8-103">A VirtualWan társított összes VpnServerConfigurations listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="428b8-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="428b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="428b8-104">SYNTAX</span></span>

### <span data-ttu-id="428b8-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="428b8-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428b8-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="428b8-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428b8-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="428b8-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="428b8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="428b8-108">DESCRIPTION</span></span>
<span data-ttu-id="428b8-109">A **Get-AzVirtualWanVpnServerConfiguration** parancsmag visszaadja az ezzel a VirtualWan társított összes VpnServerConfigurations listáját.</span><span class="sxs-lookup"><span data-stu-id="428b8-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="428b8-110">azaz minden VpnServerConfigurations, amely az VirtualWan VirutalHubs alatti bármely P2SVpnGateways van csatolva.</span><span class="sxs-lookup"><span data-stu-id="428b8-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="428b8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="428b8-111">EXAMPLES</span></span>

### <span data-ttu-id="428b8-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="428b8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="428b8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="428b8-113">PARAMETERS</span></span>

### <span data-ttu-id="428b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428b8-114">-DefaultProfile</span></span>
<span data-ttu-id="428b8-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="428b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428b8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="428b8-116">-Name</span></span>
<span data-ttu-id="428b8-117">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="428b8-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="428b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="428b8-119">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="428b8-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428b8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="428b8-120">-ResourceId</span></span>
<span data-ttu-id="428b8-121">A virtuális WAN Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="428b8-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428b8-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="428b8-122">-VirtualWanObject</span></span>
<span data-ttu-id="428b8-123">A virtuális WAN-objektum.</span><span class="sxs-lookup"><span data-stu-id="428b8-123">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="428b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428b8-124">CommonParameters</span></span>
<span data-ttu-id="428b8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="428b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428b8-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="428b8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428b8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="428b8-127">INPUTS</span></span>

### <span data-ttu-id="428b8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="428b8-128">System.String</span></span>
<span data-ttu-id="428b8-129">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="428b8-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="428b8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="428b8-130">OUTPUTS</span></span>

### <span data-ttu-id="428b8-131">Microsoft. Azure. commands. Network. models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="428b8-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="428b8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="428b8-132">NOTES</span></span>

## <span data-ttu-id="428b8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="428b8-133">RELATED LINKS</span></span>
