---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184309"
---
# <span data-ttu-id="be81e-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="be81e-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="be81e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be81e-102">SYNOPSIS</span></span>
<span data-ttu-id="be81e-103">A hálózat virtuális Appliance-erőforrásához kapcsolt virtuális gép webhelyének módosítása vagy módosítása</span><span class="sxs-lookup"><span data-stu-id="be81e-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="be81e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be81e-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be81e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="be81e-105">DESCRIPTION</span></span>
<span data-ttu-id="be81e-106">A Update-AzVirtualApplianceSite parancs módosítja a virtuális gép helyének erőforrását.</span><span class="sxs-lookup"><span data-stu-id="be81e-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="be81e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="be81e-107">EXAMPLES</span></span>

### <span data-ttu-id="be81e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="be81e-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="be81e-109">Módosítsa a virtuális gép webhely-erőforrása címének előtagját.</span><span class="sxs-lookup"><span data-stu-id="be81e-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="be81e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be81e-110">PARAMETERS</span></span>

### <span data-ttu-id="be81e-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="be81e-111">-AddresssPrefix</span></span>
<span data-ttu-id="be81e-112">A webhely címének előtagja.</span><span class="sxs-lookup"><span data-stu-id="be81e-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be81e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be81e-113">-AsJob</span></span>
<span data-ttu-id="be81e-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="be81e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be81e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be81e-115">-DefaultProfile</span></span>
<span data-ttu-id="be81e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be81e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be81e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="be81e-117">-Force</span></span>
<span data-ttu-id="be81e-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="be81e-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="be81e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be81e-119">-Name</span></span>
<span data-ttu-id="be81e-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="be81e-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be81e-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="be81e-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="be81e-122">A webhelyhez csatolt hálózati virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="be81e-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="be81e-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="be81e-123">-O365Policy</span></span>
<span data-ttu-id="be81e-124">Office 365 breakout-házirend.</span><span class="sxs-lookup"><span data-stu-id="be81e-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be81e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be81e-125">-ResourceGroupName</span></span>
<span data-ttu-id="be81e-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="be81e-126">The resource group name.</span></span>

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

### <span data-ttu-id="be81e-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="be81e-127">-Tag</span></span>
<span data-ttu-id="be81e-128">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="be81e-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="be81e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="be81e-129">-Confirm</span></span>
<span data-ttu-id="be81e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="be81e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be81e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be81e-131">-WhatIf</span></span>
<span data-ttu-id="be81e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="be81e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be81e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be81e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be81e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be81e-134">CommonParameters</span></span>
<span data-ttu-id="be81e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be81e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be81e-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="be81e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be81e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be81e-137">INPUTS</span></span>

### <span data-ttu-id="be81e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="be81e-138">System.String</span></span>

### <span data-ttu-id="be81e-139">Microsoft. Azure. commands. Network. models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="be81e-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="be81e-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="be81e-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="be81e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be81e-141">OUTPUTS</span></span>

### <span data-ttu-id="be81e-142">Microsoft. Azure. commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="be81e-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="be81e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be81e-143">NOTES</span></span>

## <span data-ttu-id="be81e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be81e-144">RELATED LINKS</span></span>
