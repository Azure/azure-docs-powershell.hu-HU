---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346566"
---
# <span data-ttu-id="8e9df-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8e9df-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="8e9df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e9df-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9df-103">Egy Azure IpGroup törlése.</span><span class="sxs-lookup"><span data-stu-id="8e9df-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="8e9df-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e9df-104">SYNTAX</span></span>

### <span data-ttu-id="8e9df-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9df-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9df-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9df-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9df-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9df-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e9df-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e9df-108">DESCRIPTION</span></span>
<span data-ttu-id="8e9df-109">Az **Remove-AzIpGroup** parancsmag töröl egy Azure IpGroup-et</span><span class="sxs-lookup"><span data-stu-id="8e9df-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="8e9df-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e9df-110">EXAMPLES</span></span>

### <span data-ttu-id="8e9df-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e9df-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="8e9df-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8e9df-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="8e9df-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="8e9df-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="8e9df-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e9df-114">PARAMETERS</span></span>

### <span data-ttu-id="8e9df-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e9df-115">-AsJob</span></span>
<span data-ttu-id="8e9df-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8e9df-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e9df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9df-117">-DefaultProfile</span></span>
<span data-ttu-id="8e9df-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e9df-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e9df-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8e9df-119">-Force</span></span>
<span data-ttu-id="8e9df-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="8e9df-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8e9df-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="8e9df-121">-IpGroup</span></span>
<span data-ttu-id="8e9df-122">Az ipGroup bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="8e9df-122">The ipGroup input object.</span></span>

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

### <span data-ttu-id="8e9df-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8e9df-123">-Name</span></span>
<span data-ttu-id="8e9df-124">Az IP-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8e9df-124">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="8e9df-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e9df-125">-PassThru</span></span>
<span data-ttu-id="8e9df-126">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="8e9df-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="8e9df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9df-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e9df-128">Az IP-csoport erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="8e9df-128">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="8e9df-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e9df-129">-ResourceId</span></span>
<span data-ttu-id="8e9df-130">Az ipgroup-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e9df-130">The ipgroup resource Id.</span></span>

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

### <span data-ttu-id="8e9df-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e9df-131">-Confirm</span></span>
<span data-ttu-id="8e9df-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e9df-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9df-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9df-133">-WhatIf</span></span>
<span data-ttu-id="8e9df-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e9df-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9df-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e9df-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9df-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9df-136">CommonParameters</span></span>
<span data-ttu-id="8e9df-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9df-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9df-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e9df-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9df-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e9df-139">INPUTS</span></span>

### <span data-ttu-id="8e9df-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8e9df-140">System.String</span></span>

### <span data-ttu-id="8e9df-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="8e9df-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="8e9df-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e9df-142">OUTPUTS</span></span>

### <span data-ttu-id="8e9df-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e9df-143">System.Boolean</span></span>

## <span data-ttu-id="8e9df-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e9df-144">NOTES</span></span>

## <span data-ttu-id="8e9df-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e9df-145">RELATED LINKS</span></span>
