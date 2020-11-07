---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: ac34f2d8c2a48010792716f183a6b86cce714294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837095"
---
# <span data-ttu-id="68d17-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68d17-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="68d17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68d17-102">SYNOPSIS</span></span>
<span data-ttu-id="68d17-103">Eltávolít egy hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="68d17-103">Removes a network profile.</span></span>

## <span data-ttu-id="68d17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68d17-104">SYNTAX</span></span>

### <span data-ttu-id="68d17-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68d17-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d17-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68d17-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d17-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68d17-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68d17-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="68d17-108">DESCRIPTION</span></span>
<span data-ttu-id="68d17-109">A **Remove-AzNetworkProfile** parancsmag akkor távolítja el a hálózati profilt, ha az alkalmazás nem tartalmaz tároló hálózati illesztőfelületet (a tároló hálózati illesztőfelület- **konfigurációval** ellentétben).</span><span class="sxs-lookup"><span data-stu-id="68d17-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="68d17-110">Példák</span><span class="sxs-lookup"><span data-stu-id="68d17-110">EXAMPLES</span></span>

### <span data-ttu-id="68d17-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="68d17-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="68d17-112">Ezzel eltávolítja a hálózati profilt a name NP1 az erőforráscsoport rg1.</span><span class="sxs-lookup"><span data-stu-id="68d17-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="68d17-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68d17-113">PARAMETERS</span></span>

### <span data-ttu-id="68d17-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68d17-114">-AsJob</span></span>
<span data-ttu-id="68d17-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="68d17-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68d17-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d17-116">-DefaultProfile</span></span>
<span data-ttu-id="68d17-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68d17-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d17-118">-Force</span><span class="sxs-lookup"><span data-stu-id="68d17-118">-Force</span></span>
<span data-ttu-id="68d17-119">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="68d17-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="68d17-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68d17-120">-InputObject</span></span>
<span data-ttu-id="68d17-121">A hálózati profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="68d17-121">Network profile object.</span></span>

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

### <span data-ttu-id="68d17-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68d17-122">-Name</span></span>
<span data-ttu-id="68d17-123">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="68d17-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="68d17-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68d17-124">-PassThru</span></span>
<span data-ttu-id="68d17-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="68d17-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="68d17-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d17-126">-ResourceGroupName</span></span>
<span data-ttu-id="68d17-127">A hálózati profil erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="68d17-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="68d17-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68d17-128">-ResourceId</span></span>
<span data-ttu-id="68d17-129">A hálózati profil Azure Resource Manager erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="68d17-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="68d17-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68d17-130">-Confirm</span></span>
<span data-ttu-id="68d17-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68d17-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d17-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d17-132">-WhatIf</span></span>
<span data-ttu-id="68d17-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68d17-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68d17-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68d17-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d17-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d17-135">CommonParameters</span></span>
<span data-ttu-id="68d17-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68d17-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d17-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68d17-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d17-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68d17-138">INPUTS</span></span>

### <span data-ttu-id="68d17-139">System. String</span><span class="sxs-lookup"><span data-stu-id="68d17-139">System.String</span></span>

### <span data-ttu-id="68d17-140">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68d17-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="68d17-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68d17-141">OUTPUTS</span></span>

### <span data-ttu-id="68d17-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68d17-142">System.Boolean</span></span>

## <span data-ttu-id="68d17-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68d17-143">NOTES</span></span>

## <span data-ttu-id="68d17-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68d17-144">RELATED LINKS</span></span>

[<span data-ttu-id="68d17-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68d17-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="68d17-146">Új – AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68d17-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="68d17-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68d17-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
