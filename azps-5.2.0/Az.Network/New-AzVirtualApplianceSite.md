---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330594"
---
# <span data-ttu-id="4fc59-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4fc59-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="4fc59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc59-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc59-103">Hozzon létre egy hálózati virtuális eszközre csatlakoztatott webhelyet.</span><span class="sxs-lookup"><span data-stu-id="4fc59-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="4fc59-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4fc59-104">SYNTAX</span></span>

### <span data-ttu-id="4fc59-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fc59-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fc59-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc59-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc59-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4fc59-107">DESCRIPTION</span></span>
<span data-ttu-id="4fc59-108">A New-AzVirtualApplianceSite parancs virtuális berendezés-webhelyet hoz létre egy hálózati virtuális eszköz típusú erőforráshoz csatlakoztatva.</span><span class="sxs-lookup"><span data-stu-id="4fc59-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="4fc59-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4fc59-109">EXAMPLES</span></span>

### <span data-ttu-id="4fc59-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4fc59-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="4fc59-111">Hozzon létre egy új virtuális eszközwebhelyet az erőforráscsoportban: testrg.</span><span class="sxs-lookup"><span data-stu-id="4fc59-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="4fc59-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fc59-112">PARAMETERS</span></span>

### <span data-ttu-id="4fc59-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4fc59-113">-AddressPrefix</span></span>
<span data-ttu-id="4fc59-114">A webhely címelőtagja.</span><span class="sxs-lookup"><span data-stu-id="4fc59-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="4fc59-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fc59-115">-AsJob</span></span>
<span data-ttu-id="4fc59-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4fc59-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fc59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc59-117">-DefaultProfile</span></span>
<span data-ttu-id="4fc59-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fc59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fc59-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4fc59-119">-Force</span></span>
<span data-ttu-id="4fc59-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="4fc59-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4fc59-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4fc59-121">-Name</span></span>
<span data-ttu-id="4fc59-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4fc59-122">The resource name.</span></span>

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

### <span data-ttu-id="4fc59-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="4fc59-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="4fc59-124">A hálózati virtuális készülék, amelyhez a webhely csatolva van.</span><span class="sxs-lookup"><span data-stu-id="4fc59-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="4fc59-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="4fc59-125">-O365Policy</span></span>
<span data-ttu-id="4fc59-126">Az Office 365 törési házirendje.</span><span class="sxs-lookup"><span data-stu-id="4fc59-126">The Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="4fc59-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc59-127">-ResourceGroupName</span></span>
<span data-ttu-id="4fc59-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4fc59-128">The resource group name.</span></span>

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

### <span data-ttu-id="4fc59-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fc59-129">-ResourceId</span></span>
<span data-ttu-id="4fc59-130">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4fc59-130">The resource id.</span></span>

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

### <span data-ttu-id="4fc59-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4fc59-131">-Tag</span></span>
<span data-ttu-id="4fc59-132">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="4fc59-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4fc59-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fc59-133">-Confirm</span></span>
<span data-ttu-id="4fc59-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4fc59-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc59-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc59-135">-WhatIf</span></span>
<span data-ttu-id="4fc59-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4fc59-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc59-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fc59-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc59-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc59-138">CommonParameters</span></span>
<span data-ttu-id="4fc59-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc59-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc59-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fc59-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc59-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fc59-141">INPUTS</span></span>

### <span data-ttu-id="4fc59-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4fc59-142">System.String</span></span>

### <span data-ttu-id="4fc59-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="4fc59-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="4fc59-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4fc59-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4fc59-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc59-145">OUTPUTS</span></span>

### <span data-ttu-id="4fc59-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4fc59-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="4fc59-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4fc59-147">NOTES</span></span>

## <span data-ttu-id="4fc59-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fc59-148">RELATED LINKS</span></span>
