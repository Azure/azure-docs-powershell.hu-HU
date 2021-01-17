---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350777"
---
# <span data-ttu-id="f19cd-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="f19cd-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="f19cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f19cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f19cd-103">Egy hálózati virtuális eszköz erőforráshoz csatlakoztatott virtuális berendezés-webhely módosítása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="f19cd-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="f19cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f19cd-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f19cd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f19cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f19cd-106">A Update-AzVirtualApplianceSite parancs módosítja a virtuális eszköz webhelyerőforrást.</span><span class="sxs-lookup"><span data-stu-id="f19cd-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="f19cd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f19cd-107">EXAMPLES</span></span>

### <span data-ttu-id="f19cd-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f19cd-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="f19cd-109">Módosítsa egy virtuális eszköz webhelyerőforrás címelőtagját.</span><span class="sxs-lookup"><span data-stu-id="f19cd-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="f19cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f19cd-110">PARAMETERS</span></span>

### <span data-ttu-id="f19cd-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="f19cd-111">-AddresssPrefix</span></span>
<span data-ttu-id="f19cd-112">A webhely címelőtagja.</span><span class="sxs-lookup"><span data-stu-id="f19cd-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="f19cd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f19cd-113">-AsJob</span></span>
<span data-ttu-id="f19cd-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f19cd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f19cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19cd-115">-DefaultProfile</span></span>
<span data-ttu-id="f19cd-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f19cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f19cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f19cd-117">-Force</span></span>
<span data-ttu-id="f19cd-118">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="f19cd-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f19cd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f19cd-119">-Name</span></span>
<span data-ttu-id="f19cd-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f19cd-120">The resource name.</span></span>

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

### <span data-ttu-id="f19cd-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="f19cd-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="f19cd-122">Hálózati virtuális készülék, amelyhez a webhely csatolva van.</span><span class="sxs-lookup"><span data-stu-id="f19cd-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="f19cd-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="f19cd-123">-O365Policy</span></span>
<span data-ttu-id="f19cd-124">Office 365-törési házirend.</span><span class="sxs-lookup"><span data-stu-id="f19cd-124">Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="f19cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="f19cd-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f19cd-126">The resource group name.</span></span>

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

### <span data-ttu-id="f19cd-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f19cd-127">-Tag</span></span>
<span data-ttu-id="f19cd-128">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="f19cd-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f19cd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f19cd-129">-Confirm</span></span>
<span data-ttu-id="f19cd-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f19cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f19cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19cd-131">-WhatIf</span></span>
<span data-ttu-id="f19cd-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f19cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19cd-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f19cd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f19cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19cd-134">CommonParameters</span></span>
<span data-ttu-id="f19cd-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19cd-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f19cd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19cd-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f19cd-137">INPUTS</span></span>

### <span data-ttu-id="f19cd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f19cd-138">System.String</span></span>

### <span data-ttu-id="f19cd-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="f19cd-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="f19cd-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f19cd-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f19cd-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f19cd-141">OUTPUTS</span></span>

### <span data-ttu-id="f19cd-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="f19cd-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="f19cd-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f19cd-143">NOTES</span></span>

## <span data-ttu-id="f19cd-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f19cd-144">RELATED LINKS</span></span>
