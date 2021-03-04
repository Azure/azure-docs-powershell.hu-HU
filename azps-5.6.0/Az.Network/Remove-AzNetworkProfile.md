---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 02a8fef51ca0689fb92d3990bf5bcc182f902549
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941585"
---
# <span data-ttu-id="4de69-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4de69-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="4de69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de69-102">SYNOPSIS</span></span>
<span data-ttu-id="4de69-103">Eltávolít egy hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="4de69-103">Removes a network profile.</span></span>

## <span data-ttu-id="4de69-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4de69-104">SYNTAX</span></span>

### <span data-ttu-id="4de69-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4de69-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4de69-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4de69-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4de69-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4de69-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de69-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4de69-108">DESCRIPTION</span></span>
<span data-ttu-id="4de69-109">A **Remove-AzNetworkProfile** parancsmag eltávolítja a hálózati profilt, ha nem jött létre tárolóhálózati felület (a tárolóhálózati felület konfigurációval ellentétben).</span><span class="sxs-lookup"><span data-stu-id="4de69-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="4de69-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4de69-110">EXAMPLES</span></span>

### <span data-ttu-id="4de69-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4de69-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="4de69-112">Ezzel eltávolítja a np1 nevű hálózati profilt az rg1 erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="4de69-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="4de69-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4de69-113">PARAMETERS</span></span>

### <span data-ttu-id="4de69-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4de69-114">-AsJob</span></span>
<span data-ttu-id="4de69-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4de69-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4de69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de69-116">-DefaultProfile</span></span>
<span data-ttu-id="4de69-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4de69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de69-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4de69-118">-Force</span></span>
<span data-ttu-id="4de69-119">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="4de69-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="4de69-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4de69-120">-InputObject</span></span>
<span data-ttu-id="4de69-121">Hálózati profilobjektum.</span><span class="sxs-lookup"><span data-stu-id="4de69-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4de69-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4de69-122">-Name</span></span>
<span data-ttu-id="4de69-123">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="4de69-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de69-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4de69-124">-PassThru</span></span>
<span data-ttu-id="4de69-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="4de69-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="4de69-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de69-126">-ResourceGroupName</span></span>
<span data-ttu-id="4de69-127">A hálózati profil erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="4de69-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de69-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4de69-128">-ResourceId</span></span>
<span data-ttu-id="4de69-129">A hálózati profil Azure-erőforrás-kezelői erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="4de69-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de69-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4de69-130">-Confirm</span></span>
<span data-ttu-id="4de69-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4de69-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de69-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de69-132">-WhatIf</span></span>
<span data-ttu-id="4de69-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4de69-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de69-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4de69-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de69-135">CommonParameters</span></span>
<span data-ttu-id="4de69-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de69-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de69-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de69-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4de69-138">INPUTS</span></span>

### <span data-ttu-id="4de69-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4de69-139">System.String</span></span>

### <span data-ttu-id="4de69-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4de69-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4de69-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4de69-141">OUTPUTS</span></span>

### <span data-ttu-id="4de69-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4de69-142">System.Boolean</span></span>

## <span data-ttu-id="4de69-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4de69-143">NOTES</span></span>

## <span data-ttu-id="4de69-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4de69-144">RELATED LINKS</span></span>

[<span data-ttu-id="4de69-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4de69-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="4de69-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4de69-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="4de69-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4de69-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
