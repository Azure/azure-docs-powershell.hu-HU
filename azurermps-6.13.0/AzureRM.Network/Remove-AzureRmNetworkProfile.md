---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680046"
---
# <span data-ttu-id="a2dc5-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a2dc5-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="a2dc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="a2dc5-103">Eltávolít egy hálózati profilt.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2dc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2dc5-104">SYNTAX</span></span>

### <span data-ttu-id="a2dc5-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="a2dc5-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2dc5-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2dc5-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2dc5-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2dc5-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2dc5-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2dc5-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2dc5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2dc5-109">DESCRIPTION</span></span>
<span data-ttu-id="a2dc5-110">A **Remove-AzureRmNetworkProfile** parancsmag akkor távolítja el a hálózati profilt, ha az alkalmazás nem tartalmaz tároló hálózati illesztőfelületet (a tároló hálózati illesztőfelület- **konfigurációval** ellentétben).</span><span class="sxs-lookup"><span data-stu-id="a2dc5-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="a2dc5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a2dc5-111">EXAMPLES</span></span>

### <span data-ttu-id="a2dc5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2dc5-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="a2dc5-113">Ezzel eltávolítja a hálózati profilt a name NP1 az erőforráscsoport rg1.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="a2dc5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2dc5-114">PARAMETERS</span></span>

### <span data-ttu-id="a2dc5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2dc5-115">-AsJob</span></span>
<span data-ttu-id="a2dc5-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a2dc5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2dc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2dc5-117">-DefaultProfile</span></span>
<span data-ttu-id="a2dc5-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2dc5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a2dc5-119">-Force</span></span>
<span data-ttu-id="a2dc5-120">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="a2dc5-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="a2dc5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2dc5-121">-InputObject</span></span>
<span data-ttu-id="a2dc5-122">A hálózati profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-122">Network profile object.</span></span>

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

### <span data-ttu-id="a2dc5-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2dc5-123">-Name</span></span>
<span data-ttu-id="a2dc5-124">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-124">The name of the network profile.</span></span>

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

### <span data-ttu-id="a2dc5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2dc5-125">-PassThru</span></span>
<span data-ttu-id="a2dc5-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a2dc5-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a2dc5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2dc5-127">-ResourceGroupName</span></span>
<span data-ttu-id="a2dc5-128">A hálózati profil erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-128">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="a2dc5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2dc5-129">-ResourceId</span></span>
<span data-ttu-id="a2dc5-130">A hálózati profil Azure Resource Manager erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-130">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="a2dc5-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2dc5-131">-Confirm</span></span>
<span data-ttu-id="a2dc5-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2dc5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2dc5-133">-WhatIf</span></span>
<span data-ttu-id="a2dc5-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2dc5-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2dc5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2dc5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2dc5-136">CommonParameters</span></span>
<span data-ttu-id="a2dc5-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2dc5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2dc5-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2dc5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2dc5-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2dc5-139">INPUTS</span></span>

### <span data-ttu-id="a2dc5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a2dc5-140">System.String</span></span>

## <span data-ttu-id="a2dc5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2dc5-141">OUTPUTS</span></span>

### <span data-ttu-id="a2dc5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2dc5-142">System.Boolean</span></span>

## <span data-ttu-id="a2dc5-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2dc5-143">NOTES</span></span>

## <span data-ttu-id="a2dc5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2dc5-144">RELATED LINKS</span></span>
