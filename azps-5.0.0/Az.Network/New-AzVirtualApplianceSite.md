---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303716"
---
# <span data-ttu-id="81786-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="81786-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="81786-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81786-102">SYNOPSIS</span></span>
<span data-ttu-id="81786-103">Hálózat virtuális készülékhez kapcsolt webhely létrehozása</span><span class="sxs-lookup"><span data-stu-id="81786-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="81786-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81786-104">SYNTAX</span></span>

### <span data-ttu-id="81786-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81786-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81786-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81786-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81786-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81786-107">DESCRIPTION</span></span>
<span data-ttu-id="81786-108">A New-AzVirtualApplianceSite parancs létrehoz egy virtuális Appliance-webhelyet, amely egy hálózat virtuális készülék-erőforráshoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="81786-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="81786-109">Példák</span><span class="sxs-lookup"><span data-stu-id="81786-109">EXAMPLES</span></span>

### <span data-ttu-id="81786-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81786-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="81786-111">Hozzon létre egy új virtuális készülék-webhelyet az erőforrás csoportban: testrg.</span><span class="sxs-lookup"><span data-stu-id="81786-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="81786-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81786-112">PARAMETERS</span></span>

### <span data-ttu-id="81786-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="81786-113">-AddressPrefix</span></span>
<span data-ttu-id="81786-114">A webhely címének előtagja.</span><span class="sxs-lookup"><span data-stu-id="81786-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="81786-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81786-115">-AsJob</span></span>
<span data-ttu-id="81786-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="81786-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81786-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81786-117">-DefaultProfile</span></span>
<span data-ttu-id="81786-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81786-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81786-119">-Force</span><span class="sxs-lookup"><span data-stu-id="81786-119">-Force</span></span>
<span data-ttu-id="81786-120">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81786-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81786-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81786-121">-Name</span></span>
<span data-ttu-id="81786-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="81786-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81786-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="81786-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="81786-124">A webhelyhez csatolt hálózati virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="81786-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="81786-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="81786-125">-O365Policy</span></span>
<span data-ttu-id="81786-126">Az Office 365 kitörési irányelvei.</span><span class="sxs-lookup"><span data-stu-id="81786-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81786-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81786-127">-ResourceGroupName</span></span>
<span data-ttu-id="81786-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="81786-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81786-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81786-129">-ResourceId</span></span>
<span data-ttu-id="81786-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="81786-130">The resource id.</span></span>

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

### <span data-ttu-id="81786-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="81786-131">-Tag</span></span>
<span data-ttu-id="81786-132">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="81786-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81786-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81786-133">-Confirm</span></span>
<span data-ttu-id="81786-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81786-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81786-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81786-135">-WhatIf</span></span>
<span data-ttu-id="81786-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81786-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81786-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81786-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81786-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81786-138">CommonParameters</span></span>
<span data-ttu-id="81786-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81786-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81786-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="81786-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81786-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81786-141">INPUTS</span></span>

### <span data-ttu-id="81786-142">System. String</span><span class="sxs-lookup"><span data-stu-id="81786-142">System.String</span></span>

### <span data-ttu-id="81786-143">Microsoft. Azure. commands. Network. models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="81786-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="81786-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="81786-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="81786-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81786-145">OUTPUTS</span></span>

### <span data-ttu-id="81786-146">Microsoft. Azure. commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="81786-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="81786-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81786-147">NOTES</span></span>

## <span data-ttu-id="81786-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81786-148">RELATED LINKS</span></span>
