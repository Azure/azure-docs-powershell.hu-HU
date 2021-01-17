---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337781"
---
# <span data-ttu-id="d0d57-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d0d57-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="d0d57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0d57-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d57-103">Szerezze be vagy sorolja fel a hálózati virtuális eszköz erőforrás(ak)hoz csatlakoztatott webhelyeket.</span><span class="sxs-lookup"><span data-stu-id="d0d57-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="d0d57-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0d57-104">SYNTAX</span></span>

### <span data-ttu-id="d0d57-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0d57-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0d57-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0d57-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0d57-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0d57-107">DESCRIPTION</span></span>
<span data-ttu-id="d0d57-108">A Get-AzVirtualApplianceSite egy vagy több hálózati virtuális eszközerőforráshoz csatlakoztatott webhelyeket kap vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="d0d57-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="d0d57-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0d57-109">EXAMPLES</span></span>

### <span data-ttu-id="d0d57-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d0d57-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="d0d57-111">Virtuális eszköz webhelyerőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="d0d57-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="d0d57-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d0d57-112">Example 2</span></span>
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

<span data-ttu-id="d0d57-113">Virtuális eszköz webhely erőforrásainak felsorolása egy hálózati virtuális eszközben.</span><span class="sxs-lookup"><span data-stu-id="d0d57-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="d0d57-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0d57-114">PARAMETERS</span></span>

### <span data-ttu-id="d0d57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d57-115">-DefaultProfile</span></span>
<span data-ttu-id="d0d57-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0d57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0d57-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d0d57-117">-Name</span></span>
<span data-ttu-id="d0d57-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d0d57-118">The resource name.</span></span>

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

### <span data-ttu-id="d0d57-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="d0d57-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="d0d57-120">A hálózati virtuális eszköz, amelyhez a webhely csatolva van.</span><span class="sxs-lookup"><span data-stu-id="d0d57-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="d0d57-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0d57-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0d57-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d0d57-122">The resource group name.</span></span>

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

### <span data-ttu-id="d0d57-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0d57-123">-ResourceId</span></span>
<span data-ttu-id="d0d57-124">A virtuális eszköz webhelyének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d0d57-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="d0d57-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d57-125">CommonParameters</span></span>
<span data-ttu-id="d0d57-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0d57-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d57-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0d57-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d57-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0d57-128">INPUTS</span></span>

### <span data-ttu-id="d0d57-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d0d57-129">System.String</span></span>

## <span data-ttu-id="d0d57-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0d57-130">OUTPUTS</span></span>

### <span data-ttu-id="d0d57-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d0d57-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="d0d57-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0d57-132">NOTES</span></span>

## <span data-ttu-id="d0d57-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0d57-133">RELATED LINKS</span></span>
