---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160955"
---
# <span data-ttu-id="d6305-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d6305-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="d6305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6305-102">SYNOPSIS</span></span>
<span data-ttu-id="d6305-103">Szerezze be vagy sorolja fel a hálózati virtuális eszköz erőforrás(ak)hoz csatlakoztatott webhelyeket.</span><span class="sxs-lookup"><span data-stu-id="d6305-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="d6305-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6305-104">SYNTAX</span></span>

### <span data-ttu-id="d6305-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6305-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6305-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6305-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6305-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6305-107">DESCRIPTION</span></span>
<span data-ttu-id="d6305-108">A Get-AzVirtualApplianceSite egy vagy több hálózati virtuális eszközerőforráshoz csatlakoztatott webhelyeket kap vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="d6305-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="d6305-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6305-109">EXAMPLES</span></span>

### <span data-ttu-id="d6305-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d6305-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="d6305-111">Virtuális eszköz webhelyerőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="d6305-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="d6305-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d6305-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="d6305-113">Virtuális eszköz webhely erőforrásainak felsorolása egy hálózati virtuális eszközben.</span><span class="sxs-lookup"><span data-stu-id="d6305-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="d6305-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6305-114">PARAMETERS</span></span>

### <span data-ttu-id="d6305-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6305-115">-DefaultProfile</span></span>
<span data-ttu-id="d6305-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6305-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6305-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d6305-117">-Name</span></span>
<span data-ttu-id="d6305-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d6305-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6305-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="d6305-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="d6305-120">A hálózati virtuális eszköz, amelyhez a webhely csatolva van.</span><span class="sxs-lookup"><span data-stu-id="d6305-120">The Network Virtual Appliance that the site is attached.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6305-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6305-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6305-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6305-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6305-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6305-123">-ResourceId</span></span>
<span data-ttu-id="d6305-124">A virtuális eszköz webhelyének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6305-124">The resource Id of the Virtual Appliance Site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6305-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6305-125">CommonParameters</span></span>
<span data-ttu-id="d6305-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6305-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6305-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6305-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6305-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6305-128">INPUTS</span></span>

### <span data-ttu-id="d6305-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d6305-129">System.String</span></span>

## <span data-ttu-id="d6305-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6305-130">OUTPUTS</span></span>

### <span data-ttu-id="d6305-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d6305-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="d6305-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6305-132">NOTES</span></span>

## <span data-ttu-id="d6305-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6305-133">RELATED LINKS</span></span>
