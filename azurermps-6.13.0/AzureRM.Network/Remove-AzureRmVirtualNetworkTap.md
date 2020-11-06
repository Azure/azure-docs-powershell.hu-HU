---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495003"
---
# <span data-ttu-id="bf7b4-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="bf7b4-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="bf7b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf7b4-102">SYNOPSIS</span></span>
<span data-ttu-id="bf7b4-103">A virtuális hálózat eltávolítása koppintással.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf7b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf7b4-104">SYNTAX</span></span>

### <span data-ttu-id="bf7b4-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf7b4-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf7b4-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf7b4-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf7b4-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf7b4-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf7b4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf7b4-108">DESCRIPTION</span></span>
<span data-ttu-id="bf7b4-109">A **Remove-AzureRmVirtualNetworkTap** parancsmag eltávolítja az Azure Virtual networkt.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="bf7b4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bf7b4-110">EXAMPLES</span></span>

### <span data-ttu-id="bf7b4-111">1. példa: virtuak-hálózat eltávolítása koppintással</span><span class="sxs-lookup"><span data-stu-id="bf7b4-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="bf7b4-112">Ez a parancs eltávolítja a VirtualNetworkTap1 az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="bf7b4-113">Mivel az *erő* paraméter nem használható, a rendszer kérni fogja a felhasználót, hogy erősítse meg ezt a lépést.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="bf7b4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf7b4-114">PARAMETERS</span></span>

### <span data-ttu-id="bf7b4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf7b4-115">-AsJob</span></span>
<span data-ttu-id="bf7b4-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bf7b4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf7b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf7b4-117">-DefaultProfile</span></span>
<span data-ttu-id="bf7b4-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf7b4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bf7b4-119">-Force</span></span>
<span data-ttu-id="bf7b4-120">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="bf7b4-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="bf7b4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf7b4-121">-InputObject</span></span>
<span data-ttu-id="bf7b4-122">Hivatkozás a VirtualNetworkTap erőforrásra</span><span class="sxs-lookup"><span data-stu-id="bf7b4-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7b4-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf7b4-123">-Name</span></span>
<span data-ttu-id="bf7b4-124">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-124">The name of the tap.</span></span>

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

### <span data-ttu-id="bf7b4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf7b4-125">-PassThru</span></span>
<span data-ttu-id="bf7b4-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf7b4-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf7b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf7b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="bf7b4-129">A virtuális hálózat erőforráscsoport neve koppintással.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="bf7b4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf7b4-130">-ResourceId</span></span>
<span data-ttu-id="bf7b4-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="bf7b4-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7b4-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf7b4-132">-Confirm</span></span>
<span data-ttu-id="bf7b4-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf7b4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf7b4-134">-WhatIf</span></span>
<span data-ttu-id="bf7b4-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf7b4-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf7b4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf7b4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf7b4-137">CommonParameters</span></span>
<span data-ttu-id="bf7b4-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf7b4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf7b4-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf7b4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf7b4-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf7b4-140">INPUTS</span></span>

### <span data-ttu-id="bf7b4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf7b4-141">System.String</span></span>

## <span data-ttu-id="bf7b4-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf7b4-142">OUTPUTS</span></span>

### <span data-ttu-id="bf7b4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf7b4-143">System.Boolean</span></span>

## <span data-ttu-id="bf7b4-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf7b4-144">NOTES</span></span>

## <span data-ttu-id="bf7b4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf7b4-145">RELATED LINKS</span></span>
