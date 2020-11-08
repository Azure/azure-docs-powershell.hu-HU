---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187253"
---
# <span data-ttu-id="27a67-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27a67-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="27a67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27a67-102">SYNOPSIS</span></span>
<span data-ttu-id="27a67-103">Eltávolít egy hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="27a67-103">Removes a network profile.</span></span>

## <span data-ttu-id="27a67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27a67-104">SYNTAX</span></span>

### <span data-ttu-id="27a67-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27a67-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a67-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27a67-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a67-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27a67-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27a67-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="27a67-108">DESCRIPTION</span></span>
<span data-ttu-id="27a67-109">A **Remove-AzNetworkProfile** parancsmag akkor távolítja el a hálózati profilt, ha az alkalmazás nem tartalmaz tároló hálózati illesztőfelületet (a tároló hálózati illesztőfelület- **konfigurációval** ellentétben).</span><span class="sxs-lookup"><span data-stu-id="27a67-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="27a67-110">Példák</span><span class="sxs-lookup"><span data-stu-id="27a67-110">EXAMPLES</span></span>

### <span data-ttu-id="27a67-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="27a67-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="27a67-112">Ezzel eltávolítja a hálózati profilt a name NP1 az erőforráscsoport rg1.</span><span class="sxs-lookup"><span data-stu-id="27a67-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="27a67-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27a67-113">PARAMETERS</span></span>

### <span data-ttu-id="27a67-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27a67-114">-AsJob</span></span>
<span data-ttu-id="27a67-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="27a67-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27a67-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a67-116">-DefaultProfile</span></span>
<span data-ttu-id="27a67-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27a67-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27a67-118">-Force</span><span class="sxs-lookup"><span data-stu-id="27a67-118">-Force</span></span>
<span data-ttu-id="27a67-119">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="27a67-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="27a67-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27a67-120">-InputObject</span></span>
<span data-ttu-id="27a67-121">A hálózati profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="27a67-121">Network profile object.</span></span>

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

### <span data-ttu-id="27a67-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27a67-122">-Name</span></span>
<span data-ttu-id="27a67-123">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="27a67-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="27a67-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27a67-124">-PassThru</span></span>
<span data-ttu-id="27a67-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="27a67-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="27a67-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a67-126">-ResourceGroupName</span></span>
<span data-ttu-id="27a67-127">A hálózati profil erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="27a67-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="27a67-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27a67-128">-ResourceId</span></span>
<span data-ttu-id="27a67-129">A hálózati profil Azure Resource Manager erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="27a67-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="27a67-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27a67-130">-Confirm</span></span>
<span data-ttu-id="27a67-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27a67-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a67-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a67-132">-WhatIf</span></span>
<span data-ttu-id="27a67-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27a67-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27a67-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27a67-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27a67-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a67-135">CommonParameters</span></span>
<span data-ttu-id="27a67-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27a67-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a67-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a67-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a67-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27a67-138">INPUTS</span></span>

### <span data-ttu-id="27a67-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27a67-139">System.String</span></span>

### <span data-ttu-id="27a67-140">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27a67-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="27a67-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27a67-141">OUTPUTS</span></span>

### <span data-ttu-id="27a67-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27a67-142">System.Boolean</span></span>

## <span data-ttu-id="27a67-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27a67-143">NOTES</span></span>

## <span data-ttu-id="27a67-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27a67-144">RELATED LINKS</span></span>

[<span data-ttu-id="27a67-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27a67-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="27a67-146">Új – AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27a67-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="27a67-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27a67-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)