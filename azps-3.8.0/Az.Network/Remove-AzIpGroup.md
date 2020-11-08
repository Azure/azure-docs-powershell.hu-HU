---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014043"
---
# <span data-ttu-id="73466-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73466-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="73466-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73466-102">SYNOPSIS</span></span>
<span data-ttu-id="73466-103">Egy Azure-IpGroup törlése</span><span class="sxs-lookup"><span data-stu-id="73466-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="73466-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73466-104">SYNTAX</span></span>

### <span data-ttu-id="73466-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73466-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73466-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73466-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73466-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73466-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73466-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="73466-108">DESCRIPTION</span></span>
<span data-ttu-id="73466-109">A **Remove-AzIpGroup** parancsmag töröl egy Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="73466-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="73466-110">Példák</span><span class="sxs-lookup"><span data-stu-id="73466-110">EXAMPLES</span></span>

### <span data-ttu-id="73466-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="73466-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="73466-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="73466-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="73466-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="73466-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="73466-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73466-114">PARAMETERS</span></span>

### <span data-ttu-id="73466-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73466-115">-AsJob</span></span>
<span data-ttu-id="73466-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="73466-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73466-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73466-117">-DefaultProfile</span></span>
<span data-ttu-id="73466-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73466-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73466-119">-Force</span><span class="sxs-lookup"><span data-stu-id="73466-119">-Force</span></span>
<span data-ttu-id="73466-120">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73466-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73466-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="73466-121">-IpGroup</span></span>
<span data-ttu-id="73466-122">A ipGroup bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="73466-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73466-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73466-123">-Name</span></span>
<span data-ttu-id="73466-124">A ipgroup neve.</span><span class="sxs-lookup"><span data-stu-id="73466-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73466-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73466-125">-PassThru</span></span>
<span data-ttu-id="73466-126">Egy olyan objektumot ad eredményül, amely azt az elemet jeleníti meg, amelyen a művelet végre van hajtva.</span><span class="sxs-lookup"><span data-stu-id="73466-126">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73466-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73466-127">-ResourceGroupName</span></span>
<span data-ttu-id="73466-128">A ipgroup erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="73466-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73466-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73466-129">-ResourceId</span></span>
<span data-ttu-id="73466-130">A ipgroup erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="73466-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73466-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73466-131">-Confirm</span></span>
<span data-ttu-id="73466-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73466-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73466-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73466-133">-WhatIf</span></span>
<span data-ttu-id="73466-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73466-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73466-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73466-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73466-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73466-136">CommonParameters</span></span>
<span data-ttu-id="73466-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73466-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73466-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="73466-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73466-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73466-139">INPUTS</span></span>

### <span data-ttu-id="73466-140">System. String</span><span class="sxs-lookup"><span data-stu-id="73466-140">System.String</span></span>

### <span data-ttu-id="73466-141">Microsoft. Azure. commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="73466-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="73466-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73466-142">OUTPUTS</span></span>

### <span data-ttu-id="73466-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73466-143">System.Boolean</span></span>

## <span data-ttu-id="73466-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73466-144">NOTES</span></span>

## <span data-ttu-id="73466-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73466-145">RELATED LINKS</span></span>
