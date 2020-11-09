---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301991"
---
# <span data-ttu-id="004d6-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="004d6-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="004d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="004d6-102">SYNOPSIS</span></span>
<span data-ttu-id="004d6-103">A hálózat virtuális készülékhez kapcsolódó erőforrás (oka) t tartalmazó webhelyek beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="004d6-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="004d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="004d6-104">SYNTAX</span></span>

### <span data-ttu-id="004d6-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="004d6-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="004d6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="004d6-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="004d6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="004d6-107">DESCRIPTION</span></span>
<span data-ttu-id="004d6-108">A Get-AzVirtualApplianceSite olyan webhelyeket kap vagy sorol fel, amelyek egy vagy több hálózati virtuális készülék-erőforráshoz kapcsolódnak.</span><span class="sxs-lookup"><span data-stu-id="004d6-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="004d6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="004d6-109">EXAMPLES</span></span>

### <span data-ttu-id="004d6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="004d6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="004d6-111">Virtuális készülék webhelyének erőforrásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="004d6-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="004d6-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="004d6-112">Example 2</span></span>
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

<span data-ttu-id="004d6-113">Virtuális Appliance-források listázása egy hálózati virtuális készüléken.</span><span class="sxs-lookup"><span data-stu-id="004d6-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="004d6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="004d6-114">PARAMETERS</span></span>

### <span data-ttu-id="004d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004d6-115">-DefaultProfile</span></span>
<span data-ttu-id="004d6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="004d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="004d6-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="004d6-117">-Name</span></span>
<span data-ttu-id="004d6-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="004d6-118">The resource name.</span></span>

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

### <span data-ttu-id="004d6-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="004d6-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="004d6-120">A webhelyhez csatolt hálózati virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="004d6-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="004d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="004d6-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="004d6-122">The resource group name.</span></span>

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

### <span data-ttu-id="004d6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="004d6-123">-ResourceId</span></span>
<span data-ttu-id="004d6-124">A virtuális gép webhelyének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="004d6-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="004d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004d6-125">CommonParameters</span></span>
<span data-ttu-id="004d6-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="004d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004d6-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="004d6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004d6-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="004d6-128">INPUTS</span></span>

### <span data-ttu-id="004d6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="004d6-129">System.String</span></span>

## <span data-ttu-id="004d6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="004d6-130">OUTPUTS</span></span>

### <span data-ttu-id="004d6-131">Microsoft. Azure. commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="004d6-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="004d6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="004d6-132">NOTES</span></span>

## <span data-ttu-id="004d6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="004d6-133">RELATED LINKS</span></span>
